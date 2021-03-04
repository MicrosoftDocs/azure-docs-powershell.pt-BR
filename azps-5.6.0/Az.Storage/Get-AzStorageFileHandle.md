---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: af5d807fcf7ad93536becd9c40df34b5e3b14220
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891249"
---
# <span data-ttu-id="0bfe5-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0bfe5-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="0bfe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bfe5-102">SYNOPSIS</span></span>
<span data-ttu-id="0bfe5-103">Lista as alças de arquivo de um compartilhamento de arquivo, um diretório de arquivos ou um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="0bfe5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0bfe5-104">SYNTAX</span></span>

### <span data-ttu-id="0bfe5-105">ShareName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0bfe5-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0bfe5-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="0bfe5-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0bfe5-107">Diretório</span><span class="sxs-lookup"><span data-stu-id="0bfe5-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="0bfe5-108">Arquivo</span><span class="sxs-lookup"><span data-stu-id="0bfe5-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="0bfe5-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0bfe5-109">DESCRIPTION</span></span>
<span data-ttu-id="0bfe5-110">O cmdlet **Get-AzStorageFileHandle** lista as alças de arquivo de um compartilhamento de arquivos ou diretório de arquivo ou um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="0bfe5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0bfe5-111">EXAMPLES</span></span>

### <span data-ttu-id="0bfe5-112">Exemplo 1: listar todos os alças de arquivo em um compartilhamento de arquivos recursivamente e classificar por ClientIp e OpenTime</span><span class="sxs-lookup"><span data-stu-id="0bfe5-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="0bfe5-113">Este comando lista as alças de arquivo em um compartilhamento de arquivos e classificar a saída por ClientIp, em seguida, por OpenTime.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="0bfe5-114">Exemplo 2: Listar os dois primeiros alças de arquivo em um diretório de arquivos recursivamente</span><span class="sxs-lookup"><span data-stu-id="0bfe5-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="0bfe5-115">Este comando lista os dois primeiros alças de arquivo em um diretório de arquivos recursivamente .</span><span class="sxs-lookup"><span data-stu-id="0bfe5-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="0bfe5-116">Exemplo 3: Listar as alças do 3º ao 6º arquivo em um arquivo</span><span class="sxs-lookup"><span data-stu-id="0bfe5-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="0bfe5-117">Este comando lista as alças do 3º ao 6º arquivo em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="0bfe5-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0bfe5-118">PARAMETERS</span></span>

### <span data-ttu-id="0bfe5-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0bfe5-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0bfe5-120">O tempo máximo de execução do lado do cliente para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-120">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0bfe5-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0bfe5-122">A quantidade total de tarefas assíncronas simultâneas.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="0bfe5-123">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-123">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-124">-Context</span><span class="sxs-lookup"><span data-stu-id="0bfe5-124">-Context</span></span>
<span data-ttu-id="0bfe5-125">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="0bfe5-125">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bfe5-126">-DefaultProfile</span></span>
<span data-ttu-id="0bfe5-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-128">-Directory</span><span class="sxs-lookup"><span data-stu-id="0bfe5-128">-Directory</span></span>
<span data-ttu-id="0bfe5-129">O objeto CloudFileDirectory indicava a pasta base onde os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-130">-File</span><span class="sxs-lookup"><span data-stu-id="0bfe5-130">-File</span></span>
<span data-ttu-id="0bfe5-131">O objeto CloudFile indicou o arquivo para listar Identificador de Arquivo.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-131">CloudFile object indicated the file to list File Handles.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-132">-Path</span><span class="sxs-lookup"><span data-stu-id="0bfe5-132">-Path</span></span>
<span data-ttu-id="0bfe5-133">Caminho para um arquivo/diretório existente.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-134">-Recursivo</span><span class="sxs-lookup"><span data-stu-id="0bfe5-134">-Recursive</span></span>
<span data-ttu-id="0bfe5-135">Lista lida com recursivamente.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-135">List handles Recursively.</span></span>
<span data-ttu-id="0bfe5-136">Só funciona no Diretório de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-136">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0bfe5-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0bfe5-138">O tempo de tempo de servidor para cada solicitação em segundos.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-138">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-139">-Share</span><span class="sxs-lookup"><span data-stu-id="0bfe5-139">-Share</span></span>
<span data-ttu-id="0bfe5-140">O objeto CloudFileShare indicava o compartilhamento em que os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-141">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0bfe5-141">-ShareName</span></span>
<span data-ttu-id="0bfe5-142">Nome do compartilhamento de arquivos onde os arquivos/diretórios seriam listados.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-142">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-143">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="0bfe5-143">-IncludeTotalCount</span></span>
<span data-ttu-id="0bfe5-144">Relata o número de objetos no conjunto de dados (um inteiro) seguido pelos objetos.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="0bfe5-145">Se o cmdlet não puder determinar a contagem total, ele retornará 'Contagem total desconhecida'.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="0bfe5-146">Atualmente, esse parâmetro não faz nada.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-146">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-147">-Skip</span><span class="sxs-lookup"><span data-stu-id="0bfe5-147">-Skip</span></span>
<span data-ttu-id="0bfe5-148">Ignora os primeiros objetos 'n' e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-149">-First</span><span class="sxs-lookup"><span data-stu-id="0bfe5-149">-First</span></span>
<span data-ttu-id="0bfe5-150">Obtém apenas os primeiros objetos 'n'.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bfe5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bfe5-151">CommonParameters</span></span>
<span data-ttu-id="0bfe5-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bfe5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bfe5-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bfe5-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bfe5-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0bfe5-154">INPUTS</span></span>

### <span data-ttu-id="0bfe5-155">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0bfe5-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="0bfe5-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0bfe5-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="0bfe5-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0bfe5-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0bfe5-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0bfe5-158">OUTPUTS</span></span>

### <span data-ttu-id="0bfe5-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="0bfe5-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="0bfe5-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="0bfe5-160">NOTES</span></span>

## <span data-ttu-id="0bfe5-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0bfe5-161">RELATED LINKS</span></span>
