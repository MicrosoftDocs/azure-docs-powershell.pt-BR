---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageShareQuota.md
ms.openlocfilehash: 62e9fc5036c4a73335b0b68154288149e806dc4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431493"
---
# <span data-ttu-id="c97e1-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c97e1-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="c97e1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c97e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c97e1-103">Define a capacidade de armazenamento de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c97e1-103">Sets the storage capacity for a share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c97e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c97e1-104">SYNTAX</span></span>

### <span data-ttu-id="c97e1-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c97e1-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c97e1-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="c97e1-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c97e1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c97e1-107">DESCRIPTION</span></span>
<span data-ttu-id="c97e1-108">O cmdlet **set-AzureStorageShareQuota** define a capacidade de armazenamento de um compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="c97e1-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="c97e1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c97e1-109">EXAMPLES</span></span>

### <span data-ttu-id="c97e1-110">Exemplo 1: definir a capacidade de armazenamento de um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c97e1-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="c97e1-111">Esse comando define a capacidade de armazenamento de um compartilhamento chamado ContosoShare01 para 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="c97e1-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="c97e1-112">OS</span><span class="sxs-lookup"><span data-stu-id="c97e1-112">PARAMETERS</span></span>

### <span data-ttu-id="c97e1-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c97e1-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c97e1-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c97e1-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c97e1-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="c97e1-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c97e1-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="c97e1-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c97e1-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c97e1-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c97e1-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c97e1-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c97e1-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="c97e1-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c97e1-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="c97e1-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c97e1-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c97e1-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c97e1-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c97e1-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c97e1-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="c97e1-123">-Context</span></span>
<span data-ttu-id="c97e1-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c97e1-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c97e1-125">Para obter um contexto de armazenamento, use o cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="c97e1-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c97e1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97e1-126">-DefaultProfile</span></span>
<span data-ttu-id="c97e1-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c97e1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c97e1-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="c97e1-128">-Quota</span></span>
<span data-ttu-id="c97e1-129">Especifica o valor da cota em gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="c97e1-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="c97e1-130">Veja a limitação de cota em https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="c97e1-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c97e1-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c97e1-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c97e1-132">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c97e1-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c97e1-133">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="c97e1-133">-Share</span></span>
<span data-ttu-id="c97e1-134">Especifica um objeto **CloudFileShare** para representar o compartilhamento para o qual esses cmdlets definem uma cota.</span><span class="sxs-lookup"><span data-stu-id="c97e1-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="c97e1-135">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="c97e1-135">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c97e1-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c97e1-136">-ShareName</span></span>
<span data-ttu-id="c97e1-137">Especifica o nome do compartilhamento de arquivo para o qual definir uma cota.</span><span class="sxs-lookup"><span data-stu-id="c97e1-137">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c97e1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97e1-138">CommonParameters</span></span>
<span data-ttu-id="c97e1-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97e1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97e1-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97e1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97e1-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c97e1-141">INPUTS</span></span>

### <span data-ttu-id="c97e1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c97e1-142">System.String</span></span>

### <span data-ttu-id="c97e1-143">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="c97e1-143">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="c97e1-144">Parâmetros: share (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c97e1-144">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="c97e1-145">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c97e1-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c97e1-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c97e1-146">OUTPUTS</span></span>

### <span data-ttu-id="c97e1-147">Microsoft. WindowsAzure. Storage. File. fileshareproperties</span><span class="sxs-lookup"><span data-stu-id="c97e1-147">Microsoft.WindowsAzure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="c97e1-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c97e1-148">NOTES</span></span>

## <span data-ttu-id="c97e1-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c97e1-149">RELATED LINKS</span></span>

[<span data-ttu-id="c97e1-150">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c97e1-150">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="c97e1-151">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c97e1-151">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="c97e1-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c97e1-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)