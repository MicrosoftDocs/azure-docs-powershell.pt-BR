---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 870843a2cf8edc20a4de6474f35934a5d12df458
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942297"
---
# <span data-ttu-id="132c2-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="132c2-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="132c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="132c2-102">SYNOPSIS</span></span>
<span data-ttu-id="132c2-103">Obtém o estado de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="132c2-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="132c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="132c2-104">SYNTAX</span></span>

### <span data-ttu-id="132c2-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="132c2-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="132c2-106">Arquivos</span><span class="sxs-lookup"><span data-stu-id="132c2-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="132c2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="132c2-107">DESCRIPTION</span></span>
<span data-ttu-id="132c2-108">O cmdlet **Get-AzStorageFileCopyState** Obtém o estado de uma operação de cópia de arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="132c2-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="132c2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="132c2-109">EXAMPLES</span></span>

### <span data-ttu-id="132c2-110">Exemplo 1: obter o estado de cópia por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="132c2-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="132c2-111">Esse comando obtém o estado da operação de cópia para um arquivo que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="132c2-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="132c2-112">OS</span><span class="sxs-lookup"><span data-stu-id="132c2-112">PARAMETERS</span></span>

### <span data-ttu-id="132c2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="132c2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="132c2-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="132c2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="132c2-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="132c2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="132c2-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="132c2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="132c2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="132c2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="132c2-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="132c2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="132c2-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="132c2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="132c2-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="132c2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="132c2-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="132c2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="132c2-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="132c2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="132c2-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="132c2-123">-Context</span></span>
<span data-ttu-id="132c2-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="132c2-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="132c2-125">Para obter um contexto, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="132c2-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="132c2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132c2-126">-DefaultProfile</span></span>
<span data-ttu-id="132c2-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="132c2-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="132c2-128">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="132c2-128">-File</span></span>
<span data-ttu-id="132c2-129">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="132c2-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="132c2-130">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="132c2-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="132c2-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="132c2-131">-FilePath</span></span>
<span data-ttu-id="132c2-132">Especifica o caminho do arquivo relativo a um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="132c2-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="132c2-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="132c2-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="132c2-134">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="132c2-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="132c2-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="132c2-135">-ShareName</span></span>
<span data-ttu-id="132c2-136">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="132c2-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="132c2-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="132c2-137">-WaitForComplete</span></span>
<span data-ttu-id="132c2-138">Indica que esse cmdlet aguarda a conclusão da cópia.</span><span class="sxs-lookup"><span data-stu-id="132c2-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="132c2-139">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="132c2-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="132c2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132c2-140">CommonParameters</span></span>
<span data-ttu-id="132c2-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="132c2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132c2-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="132c2-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132c2-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="132c2-143">INPUTS</span></span>

### <span data-ttu-id="132c2-144">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="132c2-144">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="132c2-145">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="132c2-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="132c2-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="132c2-146">OUTPUTS</span></span>

### <span data-ttu-id="132c2-147">Microsoft. Azure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="132c2-147">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="132c2-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="132c2-148">NOTES</span></span>

## <span data-ttu-id="132c2-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="132c2-149">RELATED LINKS</span></span>

[<span data-ttu-id="132c2-150">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="132c2-150">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="132c2-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="132c2-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="132c2-152">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="132c2-152">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="132c2-153">Parar-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="132c2-153">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
