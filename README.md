
## FreeType Native to the PS4s OS

**Suppports PS4 Liborbis, SDL, and GLES**

Prototypes can be found here and in *proto-include.h*

When making a Stub with OOSDK or Flatz tool, making the library this name and ONLY This name
is mandatory to link against

>libSceFreetype

DO NOT MISNAME IT

Included in the folllowing system prx
>libSceFreeTypeOl.sprx

in the following syspath
>/system/common/lib/

To use this Library you first MUST load it via this before
Calling ANY Freetype Functions

>sceSysmoduleLoadModule(SCE_SYSMODULE_FREETYPE_OL);


** This currently only supports files extensions *.ttf and *.ttc**


```void FT_Set_Transform (FT_Face face, FT_Matrix* matrix, FT_Vector* delta);
int FT_New_Memory_Face(FT_Library library, const FT_Byte* file_base, FT_Long file_size, FT_Long face_index, FT_Face* aface);
int FT_Set_Char_Size(FT_Face  face, FT_F26Dot6  char_width, FT_F26Dot6 char_height, FT_UInt horz_resolution, FT_UInt  vert_resolution);
int FT_Load_Char(FT_Face face, FT_ULong  char_code, FT_Int32 load_flags);
int FT_Init_FreeType(FT_Library* alibrary);
int FT_Done_FreeType(FT_Library  library);
int FT_Done_Face(FT_Face  face);
int FT_New_Face(FT_Library   library, const char* filepathname, FT_Long  face_index, FT_Face* aface);
int FT_Load_Glyph(FT_Face   face, FT_UInt  glyph_index, u32 load_flags); 
FT_UInt FT_Get_Char_Index(FT_Face   face, FT_ULong  charcode);
int FT_Select_Charmap(FT_Face face, FT_Encoding  encoding);
int FT_Done_Glyph(FT_Glyph FT_Glyph);
int FT_Get_Glyph(FT_GlyphSlot slot, FT_Glyph* aglyph);
int FT_Get_Kerning(FT_Face face, FT_UInt  left_glyph, FT_UInt  right_glyph, FT_UInt  kern_mode, FT_Vector* akerning);
int FT_Glyph_Stroke(FT_Glyph* pglyph, FT_Stroker   stroker, FT_Bool  destroy);
int FT_Glyph_StrokeBorder(FT_Glyph* pglyph, FT_Stroker   stroker, FT_Bool inside, FT_Bool  destroy);
int FT_Glyph_To_Bitmap(FT_Glyph* the_glyph, FT_Render_Mode  render_mode, FT_Vector* origin, FT_Bool destroy);
int FT_Library_SetLcdFilter(FT_Library library, FT_LcdFilter  filter);
int FT_Library_SetLcdFilterWeights(FT_Library  library, unsigned char* weights);
int FT_Stroker_Done(FT_Stroker  stroker);
int FT_Stroker_New(FT_Library  library, FT_Stroker* astroker);
int FT_Stroker_Set(FT_Stroker stroker, FT_Fixed  radius, FT_Stroker_LineCap   line_cap, FT_Stroker_LineJoin  line_join, FT_Fixed  miter_limit);

int FT_Open_Face(FT_Library library,const FT_Open_Args* args,FT_Long face_index,FT_Face* aface);
signed long FT_MulFix(FT_Long a,FT_Long b);
int FT_Select_Size(FT_Face face, FT_Int strike_index);
int FT_Render_Glyph(FT_GlyphSlot slot,FT_Render_Mode render_mode);
void FT_Outline_Transform(const FT_Outline* outline,const FT_Matrix* matrix);
int FT_Set_Charmap(FT_Face face,FT_CharMap charmap);
```


***Licensed Under FreeType License (FTL)***

[PS4 System Port of LibFreetype](https://www.freetype.org/)

