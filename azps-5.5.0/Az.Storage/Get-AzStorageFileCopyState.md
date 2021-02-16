---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118586"
---
# <span data-ttu-id="f9699-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="f9699-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="f9699-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9699-102">SYNOPSIS</span></span>
<span data-ttu-id="f9699-103">Obtém o estado de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="f9699-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="f9699-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9699-104">SYNTAX</span></span>

### <span data-ttu-id="f9699-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="f9699-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f9699-106">Arquivo</span><span class="sxs-lookup"><span data-stu-id="f9699-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9699-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9699-107">DESCRIPTION</span></span>
<span data-ttu-id="f9699-108">O cmdlet **Get-AzStorageFileCopyState** obtém o estado de uma operação de cópia de arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9699-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="f9699-109">Ele deve ser executado no arquivo de destino da cópia.</span><span class="sxs-lookup"><span data-stu-id="f9699-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="f9699-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f9699-110">EXAMPLES</span></span>

### <span data-ttu-id="f9699-111">Exemplo 1: Obter o estado da cópia por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="f9699-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="f9699-112">Esse comando obtém o estado da operação de cópia de um arquivo que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="f9699-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="f9699-113">Exemplo 2: Iniciar Cópia e pipeline para obter o status da cópia</span><span class="sxs-lookup"><span data-stu-id="f9699-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="f9699-114">O primeiro comando inicia a cópia do arquivo "contosofile" para "contosofile_copy" e saída do objeto de arquivo de desgregação.</span><span class="sxs-lookup"><span data-stu-id="f9699-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="f9699-115">O segundo comando pipeline o objeto de arquivo de desagregação para Get-AzStorageFileCopyState, para obter o estado de cópia do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f9699-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="f9699-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9699-116">PARAMETERS</span></span>

### <span data-ttu-id="f9699-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f9699-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f9699-118">Especifica o intervalo de tempo de tempo no lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="f9699-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f9699-119">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="f9699-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f9699-120">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esvaia, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="f9699-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f9699-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f9699-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f9699-122">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f9699-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f9699-123">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso local de CPU e largura de banda, especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="f9699-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f9699-124">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="f9699-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f9699-125">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="f9699-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f9699-126">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="f9699-126">The default value is 10.</span></span>

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

### <span data-ttu-id="f9699-127">-Contexto</span><span class="sxs-lookup"><span data-stu-id="f9699-127">-Context</span></span>
<span data-ttu-id="f9699-128">Especifica um contexto de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9699-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="f9699-129">Para obter um contexto, use o [cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="f9699-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="f9699-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9699-130">-DefaultProfile</span></span>
<span data-ttu-id="f9699-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9699-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9699-132">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="f9699-132">-File</span></span>
<span data-ttu-id="f9699-133">Especifica um objeto **CloudFile.**</span><span class="sxs-lookup"><span data-stu-id="f9699-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="f9699-134">Você pode criar um arquivo na nuvem ou obter um usando o cmdlet Get-AzStorageFile nuvem.</span><span class="sxs-lookup"><span data-stu-id="f9699-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="f9699-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="f9699-135">-FilePath</span></span>
<span data-ttu-id="f9699-136">Especifica o caminho do arquivo em relação a um compartilhamento de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9699-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9699-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f9699-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f9699-138">Especifica a duração do período de tempo de tempo para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="f9699-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f9699-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f9699-139">-ShareName</span></span>
<span data-ttu-id="f9699-140">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="f9699-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="f9699-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="f9699-141">-WaitForComplete</span></span>
<span data-ttu-id="f9699-142">Indica que esse cmdlet aguarda a cópia ser finalada.</span><span class="sxs-lookup"><span data-stu-id="f9699-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="f9699-143">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f9699-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="f9699-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9699-144">CommonParameters</span></span>
<span data-ttu-id="f9699-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9699-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9699-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9699-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9699-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="f9699-147">INPUTS</span></span>

### <span data-ttu-id="f9699-148">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="f9699-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="f9699-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9699-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f9699-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="f9699-150">OUTPUTS</span></span>

### <span data-ttu-id="f9699-151">Microsoft.Azure.Storage.File.CopyState</span><span class="sxs-lookup"><span data-stu-id="f9699-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="f9699-152">Notas</span><span class="sxs-lookup"><span data-stu-id="f9699-152">NOTES</span></span>

## <span data-ttu-id="f9699-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9699-153">RELATED LINKS</span></span>

[<span data-ttu-id="f9699-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f9699-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="f9699-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9699-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="f9699-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f9699-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="f9699-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="f9699-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
