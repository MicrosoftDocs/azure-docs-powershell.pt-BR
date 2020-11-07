---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecopystate
schema: 2.0.0
ms.openlocfilehash: 61e633bc0890a8971b0be9d1b5950d990d32e8f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785828"
---
# <span data-ttu-id="5f5c5-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="5f5c5-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="5f5c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f5c5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f5c5-103">Obtém o estado de uma operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f5c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5f5c5-104">SYNTAX</span></span>

### <span data-ttu-id="5f5c5-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="5f5c5-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5f5c5-106">Arquivos</span><span class="sxs-lookup"><span data-stu-id="5f5c5-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f5c5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5f5c5-107">DESCRIPTION</span></span>
<span data-ttu-id="5f5c5-108">O cmdlet **Get-AzureStorageFileCopyState** Obtém o estado de uma operação de cópia de arquivo de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="5f5c5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5f5c5-109">EXAMPLES</span></span>

### <span data-ttu-id="5f5c5-110">Exemplo 1: obter o estado de cópia por nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="5f5c5-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="5f5c5-111">Esse comando obtém o estado da operação de cópia para um arquivo que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="5f5c5-112">OS</span><span class="sxs-lookup"><span data-stu-id="5f5c5-112">PARAMETERS</span></span>

### <span data-ttu-id="5f5c5-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f5c5-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5f5c5-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5f5c5-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5f5c5-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="5f5c5-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5f5c5-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5f5c5-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5f5c5-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5f5c5-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5f5c5-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5f5c5-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-122">The default value is 10.</span></span>

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

### <span data-ttu-id="5f5c5-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="5f5c5-123">-Context</span></span>
<span data-ttu-id="5f5c5-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="5f5c5-125">Para obter um contexto, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="5f5c5-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="5f5c5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f5c5-126">-DefaultProfile</span></span>
<span data-ttu-id="5f5c5-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f5c5-128">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="5f5c5-128">-File</span></span>
<span data-ttu-id="5f5c5-129">Especifica um objeto **cloudfile** .</span><span class="sxs-lookup"><span data-stu-id="5f5c5-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="5f5c5-130">Você pode criar um arquivo de nuvem ou obter um usando o cmdlet Get-AzureStorageFile.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f5c5-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="5f5c5-131">-FilePath</span></span>
<span data-ttu-id="5f5c5-132">Especifica o caminho do arquivo relativo a um compartilhamento de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="5f5c5-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5f5c5-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5f5c5-134">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="5f5c5-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5f5c5-135">-ShareName</span></span>
<span data-ttu-id="5f5c5-136">Especifica o nome de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="5f5c5-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="5f5c5-137">-WaitForComplete</span></span>
<span data-ttu-id="5f5c5-138">Indica que esse cmdlet aguarda a conclusão da cópia.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="5f5c5-139">Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="5f5c5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f5c5-140">CommonParameters</span></span>
<span data-ttu-id="5f5c5-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f5c5-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f5c5-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f5c5-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5f5c5-143">INPUTS</span></span>

### <span data-ttu-id="5f5c5-144">Microsoft. WindowsAzure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="5f5c5-144">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="5f5c5-145">Parâmetros: File (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f5c5-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="5f5c5-146">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f5c5-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5f5c5-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5f5c5-147">OUTPUTS</span></span>

### <span data-ttu-id="5f5c5-148">Microsoft. WindowsAzure. Storage. File. Cloudfile</span><span class="sxs-lookup"><span data-stu-id="5f5c5-148">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="5f5c5-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5f5c5-149">NOTES</span></span>

## <span data-ttu-id="5f5c5-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f5c5-150">RELATED LINKS</span></span>

[<span data-ttu-id="5f5c5-151">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="5f5c5-151">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="5f5c5-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5f5c5-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5f5c5-153">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5f5c5-153">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="5f5c5-154">Parar-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="5f5c5-154">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)
