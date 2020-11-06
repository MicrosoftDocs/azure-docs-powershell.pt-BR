---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: ff7ac13080d3d5cb717cf7efbff322cabf83cc3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428818"
---
# <span data-ttu-id="da837-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="da837-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="da837-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da837-102">SYNOPSIS</span></span>
<span data-ttu-id="da837-103">Importa dados de BLOBs para o cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="da837-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da837-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da837-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da837-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da837-105">DESCRIPTION</span></span>
<span data-ttu-id="da837-106">O cmdlet **Import-AzureRmRedisCache** importa dados de BLOBs para o Azure Redis cache.</span><span class="sxs-lookup"><span data-stu-id="da837-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="da837-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da837-107">EXAMPLES</span></span>

### <span data-ttu-id="da837-108">Exemplo 1: importar dados</span><span class="sxs-lookup"><span data-stu-id="da837-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="da837-109">Esse comando importa dados do blob especificado pela URL SAS para o cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="da837-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="da837-110">OS</span><span class="sxs-lookup"><span data-stu-id="da837-110">PARAMETERS</span></span>

### <span data-ttu-id="da837-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da837-111">-DefaultProfile</span></span>
<span data-ttu-id="da837-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="da837-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da837-113">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="da837-113">-Files</span></span>
<span data-ttu-id="da837-114">Especifica as URLs de SAS de BLOBs cujo conteúdo esse cmdlet importa para o cache.</span><span class="sxs-lookup"><span data-stu-id="da837-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="da837-115">Você pode gerar as URLs de SAS usando os seguintes comandos do PowerShell:</span><span class="sxs-lookup"><span data-stu-id="da837-115">You can generate the SAS URLs using the following PowerShell commands:</span></span>

<span data-ttu-id="da837-116">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storagename"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="da837-116">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="da837-117">$sasKeyForBlob = New-AzureStorageBlobSASToken-container "ContainerName"-blob "blobname"-Permission "rwdl"-StartTime ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-contexto $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="da837-117">$sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span>

<span data-ttu-id="da837-118">Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "CacheName"-Files ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="da837-118">Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da837-119">-Force</span><span class="sxs-lookup"><span data-stu-id="da837-119">-Force</span></span>
<span data-ttu-id="da837-120">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="da837-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da837-121">-Format</span><span class="sxs-lookup"><span data-stu-id="da837-121">-Format</span></span>
<span data-ttu-id="da837-122">Especifica o formato do blob.</span><span class="sxs-lookup"><span data-stu-id="da837-122">Specifies the format of the blob.</span></span>
<span data-ttu-id="da837-123">Atualmente, o RDB é o único formato com suporte.</span><span class="sxs-lookup"><span data-stu-id="da837-123">Currently rdb is the only supported format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da837-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="da837-124">-Name</span></span>
<span data-ttu-id="da837-125">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="da837-125">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da837-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da837-126">-PassThru</span></span>
<span data-ttu-id="da837-127">Indica que esse cmdlet retorna um booliano que indica se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="da837-127">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="da837-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="da837-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da837-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da837-129">-ResourceGroupName</span></span>
<span data-ttu-id="da837-130">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="da837-130">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da837-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="da837-131">-Confirm</span></span>
<span data-ttu-id="da837-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da837-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da837-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da837-133">-WhatIf</span></span>
<span data-ttu-id="da837-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="da837-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da837-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="da837-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da837-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da837-136">CommonParameters</span></span>
<span data-ttu-id="da837-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da837-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da837-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da837-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da837-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da837-139">INPUTS</span></span>

### <span data-ttu-id="da837-140">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="da837-140">None</span></span>
<span data-ttu-id="da837-141">Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.</span><span class="sxs-lookup"><span data-stu-id="da837-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="da837-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da837-142">OUTPUTS</span></span>

### <span data-ttu-id="da837-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="da837-143">None</span></span>

## <span data-ttu-id="da837-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da837-144">NOTES</span></span>
* <span data-ttu-id="da837-145">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, Redis, cache, Web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="da837-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="da837-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da837-146">RELATED LINKS</span></span>

[<span data-ttu-id="da837-147">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="da837-147">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="da837-148">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="da837-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="da837-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="da837-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="da837-150">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="da837-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="da837-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="da837-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


