---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 2a9c2870e0ce33b93d3013e84e7de3642b42708c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258539"
---
# <span data-ttu-id="5d00b-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="5d00b-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="5d00b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5d00b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d00b-103">Atualize o estado de um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d00b-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="5d00b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5d00b-104">SYNTAX</span></span>

### <span data-ttu-id="5d00b-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5d00b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d00b-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d00b-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d00b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d00b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d00b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5d00b-108">DESCRIPTION</span></span>
<span data-ttu-id="5d00b-109">Esse cmdlet atualiza o estado de um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="5d00b-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="5d00b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5d00b-110">EXAMPLES</span></span>

### <span data-ttu-id="5d00b-111">Exemplo 1: habilitar a proteção de limpeza</span><span class="sxs-lookup"><span data-stu-id="5d00b-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="5d00b-112">Habilita a proteção de limpeza usando a sintaxe de tubulação.</span><span class="sxs-lookup"><span data-stu-id="5d00b-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="5d00b-113">Exemplo 2: habilitar a autorização do RBAC</span><span class="sxs-lookup"><span data-stu-id="5d00b-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="5d00b-114">Habilita a autorização RBAC usando a sintaxe de tubulação.</span><span class="sxs-lookup"><span data-stu-id="5d00b-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="5d00b-115">Exemplo 3: definir marcas</span><span class="sxs-lookup"><span data-stu-id="5d00b-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="5d00b-116">Define as marcas de um cofre de chaves chamado $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="5d00b-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="5d00b-117">Exemplo 4: limpar marcas</span><span class="sxs-lookup"><span data-stu-id="5d00b-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="5d00b-118">Exclui todas as marcas de um cofre de chaves chamado $keyVaultName.</span><span class="sxs-lookup"><span data-stu-id="5d00b-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="5d00b-119">OS</span><span class="sxs-lookup"><span data-stu-id="5d00b-119">PARAMETERS</span></span>

### <span data-ttu-id="5d00b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d00b-120">-DefaultProfile</span></span>
<span data-ttu-id="5d00b-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5d00b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d00b-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="5d00b-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="5d00b-123">Habilite a funcionalidade de proteção de limpeza para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5d00b-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="5d00b-124">Uma vez habilitado, ele não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5d00b-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="5d00b-125">Requer que o soft-Delete esteja ativado.</span><span class="sxs-lookup"><span data-stu-id="5d00b-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="5d00b-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="5d00b-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="5d00b-127">Habilite ou desabilite este cofre de chaves para autorizar ações de dados pelo controle de acesso baseado em função (RBAC).</span><span class="sxs-lookup"><span data-stu-id="5d00b-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d00b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d00b-128">-InputObject</span></span>
<span data-ttu-id="5d00b-129">Objeto do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5d00b-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d00b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d00b-130">-ResourceGroupName</span></span>
<span data-ttu-id="5d00b-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d00b-131">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d00b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d00b-132">-ResourceId</span></span>
<span data-ttu-id="5d00b-133">ID do recurso do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5d00b-133">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d00b-134">-Marca</span><span class="sxs-lookup"><span data-stu-id="5d00b-134">-Tag</span></span>
<span data-ttu-id="5d00b-135">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="5d00b-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d00b-136">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="5d00b-136">-VaultName</span></span>
<span data-ttu-id="5d00b-137">Nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5d00b-137">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d00b-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5d00b-138">-Confirm</span></span>
<span data-ttu-id="5d00b-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d00b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d00b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d00b-140">-WhatIf</span></span>
<span data-ttu-id="5d00b-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5d00b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d00b-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5d00b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d00b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d00b-143">CommonParameters</span></span>
<span data-ttu-id="5d00b-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d00b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d00b-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d00b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d00b-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5d00b-146">INPUTS</span></span>

### <span data-ttu-id="5d00b-147">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5d00b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5d00b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5d00b-148">System.String</span></span>

## <span data-ttu-id="5d00b-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5d00b-149">OUTPUTS</span></span>

### <span data-ttu-id="5d00b-150">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5d00b-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="5d00b-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5d00b-151">NOTES</span></span>

## <span data-ttu-id="5d00b-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5d00b-152">RELATED LINKS</span></span>
