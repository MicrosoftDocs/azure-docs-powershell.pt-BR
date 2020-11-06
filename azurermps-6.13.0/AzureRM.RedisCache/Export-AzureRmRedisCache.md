---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: ceba71f729de627e0e7231b9c295d0cad1ccc105
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609384"
---
# <span data-ttu-id="55f4d-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="55f4d-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="55f4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="55f4d-103">Exporta dados do Azure Redis cache para um contêiner.</span><span class="sxs-lookup"><span data-stu-id="55f4d-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55f4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55f4d-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55f4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="55f4d-106">O cmdlet **Export-AzureRmRedisCache** exporta dados do Azure Redis cache para um contêiner.</span><span class="sxs-lookup"><span data-stu-id="55f4d-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="55f4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55f4d-107">EXAMPLES</span></span>

### <span data-ttu-id="55f4d-108">Exemplo 1: exportar dados</span><span class="sxs-lookup"><span data-stu-id="55f4d-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="55f4d-109">Esse comando exporta dados de uma instância de cache do Azure Redis para o contêiner especificado pela URL SAS.</span><span class="sxs-lookup"><span data-stu-id="55f4d-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="55f4d-110">OS</span><span class="sxs-lookup"><span data-stu-id="55f4d-110">PARAMETERS</span></span>

### <span data-ttu-id="55f4d-111">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="55f4d-111">-Container</span></span>
<span data-ttu-id="55f4d-112">Especifica a URL da SAS de serviço do contêiner em que esse cmdlet exporta dados.</span><span class="sxs-lookup"><span data-stu-id="55f4d-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="55f4d-113">Você pode gerar uma URL de serviço SAS usando os seguintes comandos do PowerShell: $storageAccountContext = New-AzureStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key" $sasKeyForContainer = New-AzureStorageContainerSASToken-Name "ContainerName"-Permission "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Context $storageAccountContext-FullUri Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "CacheName"-prefix "blobprefix"-container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="55f4d-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f4d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f4d-114">-DefaultProfile</span></span>
<span data-ttu-id="55f4d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55f4d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55f4d-116">-Format</span><span class="sxs-lookup"><span data-stu-id="55f4d-116">-Format</span></span>
<span data-ttu-id="55f4d-117">Especifica um formato para o blob.</span><span class="sxs-lookup"><span data-stu-id="55f4d-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="55f4d-118">Atualmente, o RDB é o único formato com suporte.</span><span class="sxs-lookup"><span data-stu-id="55f4d-118">Currently rdb is the only supported format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f4d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="55f4d-119">-Name</span></span>
<span data-ttu-id="55f4d-120">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="55f4d-120">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f4d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55f4d-121">-PassThru</span></span>
<span data-ttu-id="55f4d-122">Indica que esse cmdlet retorna um booliano que indica se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="55f4d-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="55f4d-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="55f4d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55f4d-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="55f4d-124">-Prefix</span></span>
<span data-ttu-id="55f4d-125">Especifica um prefixo a ser usado para nomes de BLOB.</span><span class="sxs-lookup"><span data-stu-id="55f4d-125">Specifies a prefix to use for blob names.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f4d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55f4d-126">-ResourceGroupName</span></span>
<span data-ttu-id="55f4d-127">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="55f4d-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f4d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="55f4d-128">-Confirm</span></span>
<span data-ttu-id="55f4d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55f4d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f4d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f4d-130">-WhatIf</span></span>
<span data-ttu-id="55f4d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="55f4d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55f4d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="55f4d-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f4d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f4d-133">CommonParameters</span></span>
<span data-ttu-id="55f4d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55f4d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f4d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55f4d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f4d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55f4d-136">INPUTS</span></span>

### <span data-ttu-id="55f4d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="55f4d-137">System.String</span></span>

## <span data-ttu-id="55f4d-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55f4d-138">OUTPUTS</span></span>

### <span data-ttu-id="55f4d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="55f4d-139">System.Boolean</span></span>

## <span data-ttu-id="55f4d-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55f4d-140">NOTES</span></span>
* <span data-ttu-id="55f4d-141">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="55f4d-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="55f4d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55f4d-142">RELATED LINKS</span></span>

[<span data-ttu-id="55f4d-143">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="55f4d-143">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="55f4d-144">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="55f4d-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="55f4d-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="55f4d-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="55f4d-146">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="55f4d-146">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="55f4d-147">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="55f4d-147">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


