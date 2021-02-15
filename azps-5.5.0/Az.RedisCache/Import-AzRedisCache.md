---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 1f51f156a0f45b014e9ff521adb959bdbd86bef7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112669"
---
# <span data-ttu-id="08260-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08260-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="08260-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08260-102">SYNOPSIS</span></span>
<span data-ttu-id="08260-103">Importa dados de blobs para o Cache de Redis do Azure.</span><span class="sxs-lookup"><span data-stu-id="08260-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="08260-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08260-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08260-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="08260-105">DESCRIPTION</span></span>
<span data-ttu-id="08260-106">O cmdlet **Import-AzRedisCache** importa dados de blobs para o Cache Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="08260-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="08260-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08260-107">EXAMPLES</span></span>

### <span data-ttu-id="08260-108">Exemplo 1: Importar dados</span><span class="sxs-lookup"><span data-stu-id="08260-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="08260-109">Esse comando importa dados do blob especificado pela URL do SAS para o Cache do Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="08260-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="08260-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08260-110">PARAMETERS</span></span>

### <span data-ttu-id="08260-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08260-111">-DefaultProfile</span></span>
<span data-ttu-id="08260-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="08260-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08260-113">-Arquivos</span><span class="sxs-lookup"><span data-stu-id="08260-113">-Files</span></span>
<span data-ttu-id="08260-114">Especifica as URLs SAS de blobs cujo conteúdo este cmdlet importa para o cache.</span><span class="sxs-lookup"><span data-stu-id="08260-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="08260-115">Você pode gerar as URLs do SAS usando os seguintes comandos do PowerShell: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now). AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="08260-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="08260-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="08260-116">-Force</span></span>
<span data-ttu-id="08260-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="08260-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08260-118">-Formatar</span><span class="sxs-lookup"><span data-stu-id="08260-118">-Format</span></span>
<span data-ttu-id="08260-119">Especifica o formato do blob.</span><span class="sxs-lookup"><span data-stu-id="08260-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="08260-120">Atualmente, rdb é o único formato com suporte.</span><span class="sxs-lookup"><span data-stu-id="08260-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="08260-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="08260-121">-Name</span></span>
<span data-ttu-id="08260-122">Especifica o nome de um cache.</span><span class="sxs-lookup"><span data-stu-id="08260-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="08260-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08260-123">-PassThru</span></span>
<span data-ttu-id="08260-124">Indica que esse cmdlet retorna um boolano que indica se a operação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="08260-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="08260-125">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="08260-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08260-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08260-126">-ResourceGroupName</span></span>
<span data-ttu-id="08260-127">Especifica o nome do grupo de recursos que contém o cache.</span><span class="sxs-lookup"><span data-stu-id="08260-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="08260-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="08260-128">-Confirm</span></span>
<span data-ttu-id="08260-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08260-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08260-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08260-130">-WhatIf</span></span>
<span data-ttu-id="08260-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="08260-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08260-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08260-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08260-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08260-133">CommonParameters</span></span>
<span data-ttu-id="08260-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08260-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08260-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08260-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08260-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="08260-136">INPUTS</span></span>

### <span data-ttu-id="08260-137">System.String</span><span class="sxs-lookup"><span data-stu-id="08260-137">System.String</span></span>

### <span data-ttu-id="08260-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="08260-138">System.String[]</span></span>

## <span data-ttu-id="08260-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="08260-139">OUTPUTS</span></span>

### <span data-ttu-id="08260-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="08260-140">System.Boolean</span></span>

## <span data-ttu-id="08260-141">Notas</span><span class="sxs-lookup"><span data-stu-id="08260-141">NOTES</span></span>
* <span data-ttu-id="08260-142">Palavras-chave: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, site</span><span class="sxs-lookup"><span data-stu-id="08260-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="08260-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08260-143">RELATED LINKS</span></span>

[<span data-ttu-id="08260-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08260-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="08260-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08260-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="08260-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08260-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="08260-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08260-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="08260-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08260-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


