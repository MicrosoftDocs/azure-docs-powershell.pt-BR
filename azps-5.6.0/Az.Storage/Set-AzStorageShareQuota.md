---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: 132ad47cd52f258b78ac944342d86979a69abbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892595"
---
# <span data-ttu-id="4ede0-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="4ede0-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="4ede0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ede0-102">SYNOPSIS</span></span>
<span data-ttu-id="4ede0-103">Define a capacidade de armazenamento para um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="4ede0-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="4ede0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4ede0-104">SYNTAX</span></span>

### <span data-ttu-id="4ede0-105">ShareName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4ede0-105">ShareName (Default)</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4ede0-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="4ede0-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ede0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4ede0-107">DESCRIPTION</span></span>
<span data-ttu-id="4ede0-108">O cmdlet **Set-AzStorageShareQuota** define a capacidade de armazenamento de um compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="4ede0-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="4ede0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ede0-109">EXAMPLES</span></span>

### <span data-ttu-id="4ede0-110">Exemplo 1: definir a capacidade de armazenamento de um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="4ede0-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="4ede0-111">Este comando define a capacidade de armazenamento de um compartilhamento chamado ContosoShare01 como 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="4ede0-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="4ede0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4ede0-112">PARAMETERS</span></span>

### <span data-ttu-id="4ede0-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4ede0-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4ede0-114">Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="4ede0-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4ede0-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4ede0-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4ede0-116">Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="4ede0-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4ede0-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4ede0-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4ede0-118">Especifica o máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4ede0-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4ede0-119">Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="4ede0-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4ede0-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="4ede0-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4ede0-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="4ede0-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4ede0-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="4ede0-122">The default value is 10.</span></span>

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

### <span data-ttu-id="4ede0-123">-Context</span><span class="sxs-lookup"><span data-stu-id="4ede0-123">-Context</span></span>
<span data-ttu-id="4ede0-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="4ede0-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4ede0-125">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="4ede0-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4ede0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ede0-126">-DefaultProfile</span></span>
<span data-ttu-id="4ede0-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ede0-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ede0-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="4ede0-128">-Quota</span></span>
<span data-ttu-id="4ede0-129">Especifica o valor da cota em gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="4ede0-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="4ede0-130">Consulte a limitação de cota em https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="4ede0-130">See the quota limitation in https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: QuotaGiB

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ede0-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4ede0-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4ede0-132">Especifica a duração do período de tempo de duração da parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="4ede0-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4ede0-133">-Share</span><span class="sxs-lookup"><span data-stu-id="4ede0-133">-Share</span></span>
<span data-ttu-id="4ede0-134">Especifica um **objeto CloudFileShare** para representar o compartilhamento para o qual este cmdlets define uma cota.</span><span class="sxs-lookup"><span data-stu-id="4ede0-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="4ede0-135">Para obter um **objeto CloudFileShare,** use Get-AzStorageShare cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ede0-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="4ede0-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4ede0-136">-ShareName</span></span>
<span data-ttu-id="4ede0-137">Especifica o nome do compartilhamento de arquivos para o qual definir uma cota.</span><span class="sxs-lookup"><span data-stu-id="4ede0-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="4ede0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ede0-138">CommonParameters</span></span>
<span data-ttu-id="4ede0-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ede0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ede0-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ede0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ede0-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ede0-141">INPUTS</span></span>

### <span data-ttu-id="4ede0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4ede0-142">System.String</span></span>

### <span data-ttu-id="4ede0-143">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="4ede0-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="4ede0-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ede0-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ede0-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4ede0-145">OUTPUTS</span></span>

### <span data-ttu-id="4ede0-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="4ede0-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="4ede0-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="4ede0-147">NOTES</span></span>

## <span data-ttu-id="4ede0-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ede0-148">RELATED LINKS</span></span>

[<span data-ttu-id="4ede0-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="4ede0-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="4ede0-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="4ede0-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="4ede0-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ede0-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
