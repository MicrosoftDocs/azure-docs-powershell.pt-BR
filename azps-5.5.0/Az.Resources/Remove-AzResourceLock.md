---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 5047ce0ebeb4f93d1d73473edbec50eaf65c6875
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118128"
---
# <span data-ttu-id="c91a5-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c91a5-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="c91a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c91a5-102">SYNOPSIS</span></span>
<span data-ttu-id="c91a5-103">Remove um bloqueio de recursos.</span><span class="sxs-lookup"><span data-stu-id="c91a5-103">Removes a resource lock.</span></span>

## <span data-ttu-id="c91a5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c91a5-104">SYNTAX</span></span>

### <span data-ttu-id="c91a5-105">ByLockId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c91a5-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c91a5-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c91a5-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c91a5-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="c91a5-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c91a5-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="c91a5-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c91a5-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="c91a5-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c91a5-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c91a5-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c91a5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c91a5-111">DESCRIPTION</span></span>
<span data-ttu-id="c91a5-112">O **cmdlet Remove-AzResourceLock** remove um bloqueio de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="c91a5-112">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="c91a5-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c91a5-113">EXAMPLES</span></span>

### <span data-ttu-id="c91a5-114">Exemplo 1: Remover um bloqueio</span><span class="sxs-lookup"><span data-stu-id="c91a5-114">Example 1: Remove a lock</span></span>
```powershell
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="c91a5-115">Esse comando remove o bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="c91a5-115">This command removes the lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="c91a5-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c91a5-116">Example 2</span></span>

<span data-ttu-id="c91a5-117">Remove um bloqueio de recursos.</span><span class="sxs-lookup"><span data-stu-id="c91a5-117">Removes a resource lock.</span></span> <span data-ttu-id="c91a5-118">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="c91a5-118">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
Remove-AzResourceLock -LockName 'ContosoSiteLock' -ResourceGroupName myresourcegroup -ResourceName '/subscriptions/00000000-0000-0000-0000-00000000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test' -ResourceType 'Microsoft.ClassicCompute/storageAccounts'
```

## <span data-ttu-id="c91a5-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c91a5-119">PARAMETERS</span></span>

### <span data-ttu-id="c91a5-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c91a5-120">-ApiVersion</span></span>
<span data-ttu-id="c91a5-121">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="c91a5-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c91a5-122">Se você não especificar uma versão, este cmdlet usará a versão disponível mais recente.</span><span class="sxs-lookup"><span data-stu-id="c91a5-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c91a5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91a5-123">-DefaultProfile</span></span>
<span data-ttu-id="c91a5-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c91a5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c91a5-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c91a5-125">-Force</span></span>
<span data-ttu-id="c91a5-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c91a5-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c91a5-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="c91a5-127">-LockId</span></span>
<span data-ttu-id="c91a5-128">Especifica a ID do bloqueio que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="c91a5-128">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91a5-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="c91a5-129">-LockName</span></span>
<span data-ttu-id="c91a5-130">Especifica o nome do cadeado que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="c91a5-130">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91a5-131">-Pré-</span><span class="sxs-lookup"><span data-stu-id="c91a5-131">-Pre</span></span>
<span data-ttu-id="c91a5-132">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="c91a5-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c91a5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c91a5-133">-ResourceGroupName</span></span>
<span data-ttu-id="c91a5-134">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="c91a5-134">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91a5-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c91a5-135">-ResourceName</span></span>
<span data-ttu-id="c91a5-136">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="c91a5-136">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="c91a5-137">Por exemplo, para especificar um banco de dados, use o seguinte formato: Banco de Dados do `/` Servidor</span><span class="sxs-lookup"><span data-stu-id="c91a5-137">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91a5-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c91a5-138">-ResourceType</span></span>
<span data-ttu-id="c91a5-139">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="c91a5-139">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91a5-140">-Escopo</span><span class="sxs-lookup"><span data-stu-id="c91a5-140">-Scope</span></span>
<span data-ttu-id="c91a5-141">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="c91a5-141">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91a5-142">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c91a5-142">-Confirm</span></span>
<span data-ttu-id="c91a5-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c91a5-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c91a5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c91a5-144">-WhatIf</span></span>
<span data-ttu-id="c91a5-145">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c91a5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c91a5-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c91a5-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c91a5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91a5-147">CommonParameters</span></span>
<span data-ttu-id="c91a5-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c91a5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c91a5-149">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c91a5-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91a5-150">Entradas</span><span class="sxs-lookup"><span data-stu-id="c91a5-150">INPUTS</span></span>

### <span data-ttu-id="c91a5-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c91a5-151">System.String</span></span>

## <span data-ttu-id="c91a5-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="c91a5-152">OUTPUTS</span></span>

### <span data-ttu-id="c91a5-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c91a5-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c91a5-154">Notas</span><span class="sxs-lookup"><span data-stu-id="c91a5-154">NOTES</span></span>

## <span data-ttu-id="c91a5-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c91a5-155">RELATED LINKS</span></span>

[<span data-ttu-id="c91a5-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c91a5-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="c91a5-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c91a5-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="c91a5-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="c91a5-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


