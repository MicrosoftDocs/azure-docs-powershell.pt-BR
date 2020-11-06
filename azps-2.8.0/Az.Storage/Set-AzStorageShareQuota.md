---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharequota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareQuota.md
ms.openlocfilehash: 095d43d41ebc2bcccb770171e668cb737fb40834
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595834"
---
# <span data-ttu-id="e88b5-101">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="e88b5-101">Set-AzStorageShareQuota</span></span>

## <span data-ttu-id="e88b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e88b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e88b5-103">Define a capacidade de armazenamento de um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e88b5-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="e88b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e88b5-104">SYNTAX</span></span>

### <span data-ttu-id="e88b5-105">Nome_do_compartilhamento</span><span class="sxs-lookup"><span data-stu-id="e88b5-105">ShareName</span></span>
```
Set-AzStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e88b5-106">Compartilhar</span><span class="sxs-lookup"><span data-stu-id="e88b5-106">Share</span></span>
```
Set-AzStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e88b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e88b5-107">DESCRIPTION</span></span>
<span data-ttu-id="e88b5-108">O cmdlet **set-AzStorageShareQuota** define a capacidade de armazenamento de um compartilhamento especificado.</span><span class="sxs-lookup"><span data-stu-id="e88b5-108">The **Set-AzStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="e88b5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e88b5-109">EXAMPLES</span></span>

### <span data-ttu-id="e88b5-110">Exemplo 1: definir a capacidade de armazenamento de um compartilhamento</span><span class="sxs-lookup"><span data-stu-id="e88b5-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="e88b5-111">Esse comando define a capacidade de armazenamento de um compartilhamento chamado ContosoShare01 para 1024 GB.</span><span class="sxs-lookup"><span data-stu-id="e88b5-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="e88b5-112">OS</span><span class="sxs-lookup"><span data-stu-id="e88b5-112">PARAMETERS</span></span>

### <span data-ttu-id="e88b5-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e88b5-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e88b5-114">Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="e88b5-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e88b5-115">Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.</span><span class="sxs-lookup"><span data-stu-id="e88b5-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e88b5-116">Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="e88b5-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e88b5-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e88b5-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e88b5-118">Especifica o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e88b5-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e88b5-119">Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.</span><span class="sxs-lookup"><span data-stu-id="e88b5-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e88b5-120">O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.</span><span class="sxs-lookup"><span data-stu-id="e88b5-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e88b5-121">Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.</span><span class="sxs-lookup"><span data-stu-id="e88b5-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e88b5-122">O valor padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="e88b5-122">The default value is 10.</span></span>

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

### <span data-ttu-id="e88b5-123">-Contexto</span><span class="sxs-lookup"><span data-stu-id="e88b5-123">-Context</span></span>
<span data-ttu-id="e88b5-124">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="e88b5-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e88b5-125">Para obter um contexto de armazenamento, use o cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="e88b5-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e88b5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88b5-126">-DefaultProfile</span></span>
<span data-ttu-id="e88b5-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e88b5-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88b5-128">-Quota</span><span class="sxs-lookup"><span data-stu-id="e88b5-128">-Quota</span></span>
<span data-ttu-id="e88b5-129">Especifica o valor da cota em gigabytes (GB).</span><span class="sxs-lookup"><span data-stu-id="e88b5-129">Specifies the quota value in gigabytes (GB).</span></span>
<span data-ttu-id="e88b5-130">Veja a limitação de cota em https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits .</span><span class="sxs-lookup"><span data-stu-id="e88b5-130">See the quota limitation in https://docs.microsoft.com/en-us/azure/azure-subscription-service-limits#azure-files-limits.</span></span> 

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

### <span data-ttu-id="e88b5-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e88b5-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e88b5-132">Especifica o comprimento do período de tempo limite para a parte do servidor de uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="e88b5-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e88b5-133">-Compartilhar</span><span class="sxs-lookup"><span data-stu-id="e88b5-133">-Share</span></span>
<span data-ttu-id="e88b5-134">Especifica um objeto **CloudFileShare** para representar o compartilhamento para o qual esses cmdlets definem uma cota.</span><span class="sxs-lookup"><span data-stu-id="e88b5-134">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="e88b5-135">Para obter um objeto **CloudFileShare** , use o cmdlet Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="e88b5-135">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e88b5-136">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e88b5-136">-ShareName</span></span>
<span data-ttu-id="e88b5-137">Especifica o nome do compartilhamento de arquivo para o qual definir uma cota.</span><span class="sxs-lookup"><span data-stu-id="e88b5-137">Specifies the name of the file share for which to set a quota.</span></span>

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

### <span data-ttu-id="e88b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88b5-138">CommonParameters</span></span>
<span data-ttu-id="e88b5-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e88b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88b5-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88b5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88b5-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e88b5-141">INPUTS</span></span>

### <span data-ttu-id="e88b5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e88b5-142">System.String</span></span>

### <span data-ttu-id="e88b5-143">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e88b5-143">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="e88b5-144">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e88b5-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e88b5-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e88b5-145">OUTPUTS</span></span>

### <span data-ttu-id="e88b5-146">Microsoft. Azure. Storage. File. fileshareproperties</span><span class="sxs-lookup"><span data-stu-id="e88b5-146">Microsoft.Azure.Storage.File.FileShareProperties</span></span>

## <span data-ttu-id="e88b5-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e88b5-147">NOTES</span></span>

## <span data-ttu-id="e88b5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e88b5-148">RELATED LINKS</span></span>

[<span data-ttu-id="e88b5-149">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e88b5-149">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="e88b5-150">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="e88b5-150">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="e88b5-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="e88b5-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)
