---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: 278afd493d66fdc817bd61b0a11e15b1c6b54391
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432759"
---
# <span data-ttu-id="e3b17-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3b17-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="e3b17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3b17-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b17-103">Importa dados de BLOBs para o cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e3b17-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3b17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3b17-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b17-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3b17-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b17-106">O cmdlet **Import-AzureRmRedisCache** importa dados de BLOBs para o Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="e3b17-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="e3b17-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3b17-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b17-108">Exemplo 1: importar dados</span><span class="sxs-lookup"><span data-stu-id="e3b17-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="e3b17-109">Esse comando importa dados do blob especificado pela URL SAS para o cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e3b17-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="e3b17-110">OS</span><span class="sxs-lookup"><span data-stu-id="e3b17-110">PARAMETERS</span></span>

### <span data-ttu-id="e3b17-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b17-111">-DefaultProfile</span></span>
<span data-ttu-id="e3b17-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b17-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3b17-113">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="e3b17-113">-Files</span></span>
<span data-ttu-id="e3b17-114">Especifica as URLs de SAS de BLOBs cujo conteúdo esse cmdlet importa para o cache.</span><span class="sxs-lookup"><span data-stu-id="e3b17-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="e3b17-115">Você pode gerar as URLs de SAS usando os seguintes comandos do PowerShell: $storageAccountContext = New-AzureStorageContext-StorageAccountName "storagename"-StorageAccountKey "" $sasKeyForBlob = New-AzureStorageBlobSASToken-container "ContainerName"-blob "blobname"-permissão "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Context $storageAccountContext-FullUri Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "CacheName"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="e3b17-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b17-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e3b17-116">-Force</span></span>
<span data-ttu-id="e3b17-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3b17-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3b17-118">-Format</span><span class="sxs-lookup"><span data-stu-id="e3b17-118">-Format</span></span>
<span data-ttu-id="e3b17-119">Especifica o formato do blob.</span><span class="sxs-lookup"><span data-stu-id="e3b17-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="e3b17-120">Atualmente, o RDB é o único formato com suporte.</span><span class="sxs-lookup"><span data-stu-id="e3b17-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="e3b17-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3b17-121">-Name</span></span>
<span data-ttu-id="e3b17-122">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="e3b17-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="e3b17-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3b17-123">-PassThru</span></span>
<span data-ttu-id="e3b17-124">Indica que esse cmdlet retorna um booliano que indica se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e3b17-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="e3b17-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e3b17-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3b17-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b17-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3b17-127">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="e3b17-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="e3b17-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e3b17-128">-Confirm</span></span>
<span data-ttu-id="e3b17-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3b17-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b17-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b17-130">-WhatIf</span></span>
<span data-ttu-id="e3b17-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3b17-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3b17-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3b17-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b17-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b17-133">CommonParameters</span></span>
<span data-ttu-id="e3b17-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3b17-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b17-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b17-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b17-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3b17-136">INPUTS</span></span>

### <span data-ttu-id="e3b17-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b17-137">System.String</span></span>

### <span data-ttu-id="e3b17-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="e3b17-138">System.String[]</span></span>

## <span data-ttu-id="e3b17-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3b17-139">OUTPUTS</span></span>

### <span data-ttu-id="e3b17-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3b17-140">System.Boolean</span></span>

## <span data-ttu-id="e3b17-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3b17-141">NOTES</span></span>
* <span data-ttu-id="e3b17-142">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="e3b17-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e3b17-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3b17-143">RELATED LINKS</span></span>

[<span data-ttu-id="e3b17-144">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3b17-144">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="e3b17-145">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3b17-145">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="e3b17-146">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3b17-146">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="e3b17-147">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3b17-147">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="e3b17-148">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="e3b17-148">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


