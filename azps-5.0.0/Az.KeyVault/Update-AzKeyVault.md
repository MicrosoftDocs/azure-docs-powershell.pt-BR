---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115276"
---
# <span data-ttu-id="d2acf-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d2acf-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="d2acf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2acf-102">SYNOPSIS</span></span>
<span data-ttu-id="d2acf-103">Atualize o estado de um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2acf-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="d2acf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2acf-104">SYNTAX</span></span>

### <span data-ttu-id="d2acf-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2acf-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2acf-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2acf-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2acf-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2acf-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2acf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2acf-108">DESCRIPTION</span></span>
<span data-ttu-id="d2acf-109">Esse cmdlet atualiza o estado de um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2acf-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="d2acf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2acf-110">EXAMPLES</span></span>

### <span data-ttu-id="d2acf-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2acf-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="d2acf-112">Habilita a proteção de limpeza usando a sintaxe de tubulação.</span><span class="sxs-lookup"><span data-stu-id="d2acf-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="d2acf-113">OS</span><span class="sxs-lookup"><span data-stu-id="d2acf-113">PARAMETERS</span></span>

### <span data-ttu-id="d2acf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2acf-114">-DefaultProfile</span></span>
<span data-ttu-id="d2acf-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2acf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2acf-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="d2acf-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="d2acf-117">Habilite a funcionalidade de proteção de limpeza para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d2acf-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="d2acf-118">Uma vez habilitado, ele não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="d2acf-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="d2acf-119">Requer que o soft-Delete esteja ativado.</span><span class="sxs-lookup"><span data-stu-id="d2acf-119">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="d2acf-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="d2acf-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="d2acf-121">Habilite ou desabilite este cofre de chaves para autorizar ações de dados pelo controle de acesso baseado em função (RBAC).</span><span class="sxs-lookup"><span data-stu-id="d2acf-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="d2acf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2acf-122">-InputObject</span></span>
<span data-ttu-id="d2acf-123">Objeto do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d2acf-123">Key vault object.</span></span>

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

### <span data-ttu-id="d2acf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2acf-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2acf-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d2acf-125">Name of the resource group.</span></span>

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

### <span data-ttu-id="d2acf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2acf-126">-ResourceId</span></span>
<span data-ttu-id="d2acf-127">ID do recurso do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d2acf-127">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="d2acf-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="d2acf-128">-VaultName</span></span>
<span data-ttu-id="d2acf-129">Nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="d2acf-129">Name of the key vault.</span></span>

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

### <span data-ttu-id="d2acf-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2acf-130">-Confirm</span></span>
<span data-ttu-id="d2acf-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2acf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2acf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2acf-132">-WhatIf</span></span>
<span data-ttu-id="d2acf-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2acf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2acf-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2acf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2acf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2acf-135">CommonParameters</span></span>
<span data-ttu-id="d2acf-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2acf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2acf-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d2acf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2acf-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2acf-138">INPUTS</span></span>

### <span data-ttu-id="d2acf-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d2acf-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d2acf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d2acf-140">System.String</span></span>

## <span data-ttu-id="d2acf-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2acf-141">OUTPUTS</span></span>

### <span data-ttu-id="d2acf-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d2acf-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="d2acf-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2acf-143">NOTES</span></span>

## <span data-ttu-id="d2acf-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2acf-144">RELATED LINKS</span></span>
