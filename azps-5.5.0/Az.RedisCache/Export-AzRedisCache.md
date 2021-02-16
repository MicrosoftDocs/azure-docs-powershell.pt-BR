---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113357"
---
# <span data-ttu-id="6eccb-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6eccb-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="6eccb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6eccb-102">SYNOPSIS</span></span>
<span data-ttu-id="6eccb-103">Exporta dados do Cache de Redis do Azure para um contêiner.</span><span class="sxs-lookup"><span data-stu-id="6eccb-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="6eccb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6eccb-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6eccb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6eccb-105">DESCRIPTION</span></span>
<span data-ttu-id="6eccb-106">O cmdlet **Export-AzRedisCache** exporta dados do Cache Azure Redis para um contêiner.</span><span class="sxs-lookup"><span data-stu-id="6eccb-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="6eccb-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6eccb-107">EXAMPLES</span></span>

### <span data-ttu-id="6eccb-108">Exemplo 1: Exportar dados</span><span class="sxs-lookup"><span data-stu-id="6eccb-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="6eccb-109">Esse comando exporta dados de uma instância do Cache de Redis do Azure para o contêiner especificado pela URL do SAS.</span><span class="sxs-lookup"><span data-stu-id="6eccb-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="6eccb-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6eccb-110">PARAMETERS</span></span>

### <span data-ttu-id="6eccb-111">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="6eccb-111">-Container</span></span>
<span data-ttu-id="6eccb-112">Especifica a URL do serviço SAS do contêiner onde este cmdlet exporta dados.</span><span class="sxs-lookup"><span data-stu-id="6eccb-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="6eccb-113">Você pode gerar uma URL do SAS de Serviço usando os seguintes comandos do PowerShell: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "nomedo contêiner" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="6eccb-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="6eccb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eccb-114">-DefaultProfile</span></span>
<span data-ttu-id="6eccb-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="6eccb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eccb-116">-Formatar</span><span class="sxs-lookup"><span data-stu-id="6eccb-116">-Format</span></span>
<span data-ttu-id="6eccb-117">Especifica um formato para o blob.</span><span class="sxs-lookup"><span data-stu-id="6eccb-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="6eccb-118">Atualmente, rdb é o único formato com suporte.</span><span class="sxs-lookup"><span data-stu-id="6eccb-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="6eccb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6eccb-119">-Name</span></span>
<span data-ttu-id="6eccb-120">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="6eccb-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="6eccb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6eccb-121">-PassThru</span></span>
<span data-ttu-id="6eccb-122">Indica que esse cmdlet retorna um boolano que indica se a operação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6eccb-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="6eccb-123">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="6eccb-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6eccb-124">-Prefixo</span><span class="sxs-lookup"><span data-stu-id="6eccb-124">-Prefix</span></span>
<span data-ttu-id="6eccb-125">Especifica um prefixo a ser usado para nomes de blob.</span><span class="sxs-lookup"><span data-stu-id="6eccb-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="6eccb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eccb-126">-ResourceGroupName</span></span>
<span data-ttu-id="6eccb-127">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="6eccb-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="6eccb-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6eccb-128">-Confirm</span></span>
<span data-ttu-id="6eccb-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eccb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eccb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eccb-130">-WhatIf</span></span>
<span data-ttu-id="6eccb-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6eccb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6eccb-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6eccb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eccb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eccb-133">CommonParameters</span></span>
<span data-ttu-id="6eccb-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eccb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eccb-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eccb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eccb-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="6eccb-136">INPUTS</span></span>

### <span data-ttu-id="6eccb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6eccb-137">System.String</span></span>

## <span data-ttu-id="6eccb-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="6eccb-138">OUTPUTS</span></span>

### <span data-ttu-id="6eccb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6eccb-139">System.Boolean</span></span>

## <span data-ttu-id="6eccb-140">Notas</span><span class="sxs-lookup"><span data-stu-id="6eccb-140">NOTES</span></span>
* <span data-ttu-id="6eccb-141">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="6eccb-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6eccb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6eccb-142">RELATED LINKS</span></span>

[<span data-ttu-id="6eccb-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6eccb-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="6eccb-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6eccb-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6eccb-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6eccb-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6eccb-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6eccb-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="6eccb-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6eccb-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


