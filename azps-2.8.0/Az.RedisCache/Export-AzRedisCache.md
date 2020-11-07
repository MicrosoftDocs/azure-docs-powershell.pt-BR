---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: ec6abf13cf4f14a8d0cdaab75d5816d87f0540ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772948"
---
# <span data-ttu-id="1f6f8-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f6f8-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="1f6f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f6f8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6f8-103">Exporta dados do Azure Redis cache para um contêiner.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="1f6f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f6f8-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f6f8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f6f8-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6f8-106">O cmdlet **Export-AzRedisCache** exporta dados do Azure Redis cache para um contêiner.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="1f6f8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f6f8-107">EXAMPLES</span></span>

### <span data-ttu-id="1f6f8-108">Exemplo 1: exportar dados</span><span class="sxs-lookup"><span data-stu-id="1f6f8-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="1f6f8-109">Esse comando exporta dados de uma instância de cache do Azure Redis para o contêiner especificado pela URL SAS.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="1f6f8-110">OS</span><span class="sxs-lookup"><span data-stu-id="1f6f8-110">PARAMETERS</span></span>

### <span data-ttu-id="1f6f8-111">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="1f6f8-111">-Container</span></span>
<span data-ttu-id="1f6f8-112">Especifica a URL da SAS de serviço do contêiner em que esse cmdlet exporta dados.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="1f6f8-113">Você pode gerar uma URL de serviço SAS usando os seguintes comandos do PowerShell: $storageAccountContext = New-AzStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key" $sasKeyForContainer = New-AzStorageContainerSASToken-Name "ContainerName"-Permission "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Context $storageAccountContext-FullUri Export-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "CacheName"-prefix "blobprefix"-container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="1f6f8-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="1f6f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6f8-114">-DefaultProfile</span></span>
<span data-ttu-id="1f6f8-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6f8-116">-Format</span><span class="sxs-lookup"><span data-stu-id="1f6f8-116">-Format</span></span>
<span data-ttu-id="1f6f8-117">Especifica um formato para o blob.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="1f6f8-118">Atualmente, o RDB é o único formato com suporte.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="1f6f8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f6f8-119">-Name</span></span>
<span data-ttu-id="1f6f8-120">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="1f6f8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f6f8-121">-PassThru</span></span>
<span data-ttu-id="1f6f8-122">Indica que esse cmdlet retorna um booliano que indica se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="1f6f8-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f6f8-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="1f6f8-124">-Prefix</span></span>
<span data-ttu-id="1f6f8-125">Especifica um prefixo a ser usado para nomes de BLOB.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="1f6f8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6f8-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f6f8-127">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="1f6f8-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f6f8-128">-Confirm</span></span>
<span data-ttu-id="1f6f8-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f6f8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f6f8-130">-WhatIf</span></span>
<span data-ttu-id="1f6f8-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f6f8-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f6f8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6f8-133">CommonParameters</span></span>
<span data-ttu-id="1f6f8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6f8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6f8-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f6f8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6f8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f6f8-136">INPUTS</span></span>

### <span data-ttu-id="1f6f8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1f6f8-137">System.String</span></span>

## <span data-ttu-id="1f6f8-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f6f8-138">OUTPUTS</span></span>

### <span data-ttu-id="1f6f8-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f6f8-139">System.Boolean</span></span>

## <span data-ttu-id="1f6f8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f6f8-140">NOTES</span></span>
* <span data-ttu-id="1f6f8-141">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="1f6f8-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1f6f8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f6f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="1f6f8-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f6f8-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="1f6f8-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f6f8-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1f6f8-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f6f8-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="1f6f8-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f6f8-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="1f6f8-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1f6f8-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)

