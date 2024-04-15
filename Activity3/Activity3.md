# Activity 3: Angular Music App Fixed Data

# Part 1: : Basic Angular Components, Events, Routes, and Data Binding

**Screenshot 1: Large screen showcasing responisve grid**
![Alt text for Screenshot 1](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/1.1.png)

**Screenshot 2: Small screen showcasing responisve grid**
![Alt text for Screenshot 2](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/1.2.png)

**Screenshot 3: Before Name Is Entered**
![Alt text for Screenshot 3](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/1.3.png)

**Screenshot 4: After Name Is Entered**
![Alt text for Screenshot 4](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/1.4.png)

**Screenshot 5: Browser dev tools with quantity and product**
![Alt text for Screenshot 5](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/1.5.png)

## Research and Insights

### Describe @Input decorator used in info.component.ts

The @Input decorator in info.component.ts is used to bind a property or function in InfoComponent to a value passed down from its parent component, allowing data to flow from the parent to the child component.

### Describe [value] used in info.component.html

[value] in info.component.html is a property binding syntax in Angular, used to bind the property of a DOM element (like an input field) to a component or directive property.

### Describe [(ngModel)] also used in info.component.html

[(ngModel)] in info.component.html is the Angular two-way data binding syntax, which binds an HTML form element's value to a component property. This allows for mutual data exchange, where changes to the component property reflect in the HTML element and vice versa.

# Part 2: Creating a Music Application – The Front End

**Screenshot 6: Initial Application Page**
![Alt text for Screenshot 6](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/2.1.png)

**Screenshot 7: GCU Homepage**
![Alt text for Screenshot 7](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/2.2.png)

**Screenshot 8: Create Album Page**
![Alt text for Screenshot 8](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/2.3.png)

**Screenshot 9: Artist List Page With New Album**
![Alt text for Screenshot 9](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/2.4.png)

**Screenshot 10: About Box**
![Alt text for Screenshot 10](https://raw.githubusercontent.com/Eli9Saavedra/CST391Public/main/Activity3/Images/2.5.png)

## Research
```typescript
import { Injectable } from '@angular/core';
import exampledata from '../../data/sample-music-data.json';
import { Album } from '../models/Album';
import { Artist } from '../models/Artist';
import { Track } from '../models/Track';

// Marks this service as available to be provided and injected as a dependency anywhere
@Injectable({ providedIn: 'root' })
export class MusicServiceService {
  // Private arrays to hold artists and albums data
  private readonly artists: Artist[] = [];
  private readonly albums: Album[] = [];

  constructor() {
    // Initialize artists and albums data on service instantiation
    this.createArtists();
    this.createAlbums();
  }

  // Method to populate the artists array
  private createArtists(): void {
    // Example artist "The Beatles" added to artists array
    this.artists.push(new Artist(0, 'The Beatles'));
  }

  // Method to populate the albums array based on sample data
  private createAlbums(): void {
    exampledata.forEach((data: any) => {
      // Filters albums for "The Beatles" and creates album and tracks objects
      if (data.artist === 'The Beatles') {
        const tracks = data.tracks.map((trackData: any) => new Track(trackData.id, trackData.number, trackData.title, trackData.lyrics, trackData.video));
        const album = new Album(data.id, data.title, data.artist, data.description, data.year, data.image, tracks);
        this.albums.push(album);
      }
    });
  }

  // Public method to get all artists
  public getArtists(): Artist[] {
    return this.artists;
  }

  // Public method to get albums by an artist
  public getAlbums(artist: string): Album[] {
    return this.albums.filter((album) => album.Artist === artist);
  }

  // Public method to get a specific album by artist and album ID
  public getAlbum(artist: string, id: number): Album | undefined {
    const album = this.albums.find((a) => a.Artist === artist && a.Id === id);
    if (album) {
      // Recreates the Album object to ensure immutability
      const tracks = album.Tracks.map((track) => new Track(track.Id, track.Number, track.Title, track.Lyrics, track.Video));
      return new Album(album.Id, album.Title, album.Artist, album.Description, album.Year, album.Image, tracks);
    }
    return undefined;
  }

  // Adds a new album to the albums array
  public createAlbum(album: Album): void {
    this.albums.push(album);
  }

  // Updates an existing album in the albums array
  public updateAlbum(album: Album): void {
    const index = this.albums.findIndex((a) => a.Id === album.Id);
    if (index !== -1) {
      this.albums.splice(index, 1, album);
    }
  }

  // Deletes an album from the albums array by ID
  public deleteAlbum(id: number): void {
    const index = this.albums.findIndex((a) => a.Id === id);
    if (index !== -1) {
      this.albums.splice(index, 1);
    }
  }
}
```