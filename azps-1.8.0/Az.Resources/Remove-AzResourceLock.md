---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceLock.md
ms.openlocfilehash: 32a3dbb458c4848a5578309593b205b4ced5be03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599331"
---
# <span data-ttu-id="296d1-101">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="296d1-101">Remove-AzResourceLock</span></span>

## <span data-ttu-id="296d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="296d1-102">SYNOPSIS</span></span>
<span data-ttu-id="296d1-103">Remove um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="296d1-103">Removes a resource lock.</span></span>

## <span data-ttu-id="296d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="296d1-104">SYNTAX</span></span>

### <span data-ttu-id="296d1-105">ByLockId (padrão)</span><span class="sxs-lookup"><span data-stu-id="296d1-105">ByLockId (Default)</span></span>
```
Remove-AzResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296d1-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="296d1-106">ByResourceGroup</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296d1-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="296d1-107">ByResourceGroupLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296d1-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="296d1-108">BySpecifiedScope</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296d1-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="296d1-109">BySubscription</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="296d1-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="296d1-110">BySubscriptionLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="296d1-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="296d1-111">ByTenantLevel</span></span>
```
Remove-AzResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="296d1-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="296d1-112">DESCRIPTION</span></span>
<span data-ttu-id="296d1-113">O cmdlet **Remove-AzResourceLock** remove um bloqueio de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="296d1-113">The **Remove-AzResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="296d1-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="296d1-114">EXAMPLES</span></span>

### <span data-ttu-id="296d1-115">Exemplo 1: remover um bloqueio</span><span class="sxs-lookup"><span data-stu-id="296d1-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="296d1-116">Esse comando Remove o bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="296d1-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="296d1-117">OS</span><span class="sxs-lookup"><span data-stu-id="296d1-117">PARAMETERS</span></span>

### <span data-ttu-id="296d1-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="296d1-118">-ApiVersion</span></span>
<span data-ttu-id="296d1-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="296d1-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="296d1-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="296d1-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="296d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="296d1-121">-DefaultProfile</span></span>
<span data-ttu-id="296d1-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="296d1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="296d1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="296d1-123">-Force</span></span>
<span data-ttu-id="296d1-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="296d1-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="296d1-125">-LockId</span><span class="sxs-lookup"><span data-stu-id="296d1-125">-LockId</span></span>
<span data-ttu-id="296d1-126">Especifica a ID do bloqueio que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="296d1-126">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="296d1-127">-Lockname</span><span class="sxs-lookup"><span data-stu-id="296d1-127">-LockName</span></span>
<span data-ttu-id="296d1-128">Especifica o nome do bloqueio que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="296d1-128">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="296d1-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="296d1-129">-Pre</span></span>
<span data-ttu-id="296d1-130">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="296d1-130">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="296d1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="296d1-131">-ResourceGroupName</span></span>
<span data-ttu-id="296d1-132">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="296d1-132">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="296d1-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="296d1-133">-ResourceName</span></span>
<span data-ttu-id="296d1-134">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="296d1-134">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="296d1-135">Por exemplo, para especificar um banco de dados, use o seguinte formato: banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="296d1-135">For instance, to specify a database, use the following format: Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="296d1-136">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="296d1-136">-ResourceType</span></span>
<span data-ttu-id="296d1-137">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="296d1-137">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="296d1-138">-Escopo</span><span class="sxs-lookup"><span data-stu-id="296d1-138">-Scope</span></span>
<span data-ttu-id="296d1-139">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="296d1-139">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="296d1-140">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="296d1-140">-TenantLevel</span></span>
<span data-ttu-id="296d1-141">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="296d1-141">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="296d1-142">-Confirme</span><span class="sxs-lookup"><span data-stu-id="296d1-142">-Confirm</span></span>
<span data-ttu-id="296d1-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="296d1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="296d1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="296d1-144">-WhatIf</span></span>
<span data-ttu-id="296d1-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="296d1-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="296d1-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="296d1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="296d1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="296d1-147">CommonParameters</span></span>
<span data-ttu-id="296d1-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="296d1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="296d1-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="296d1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="296d1-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="296d1-150">INPUTS</span></span>

### <span data-ttu-id="296d1-151">System. String</span><span class="sxs-lookup"><span data-stu-id="296d1-151">System.String</span></span>

## <span data-ttu-id="296d1-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="296d1-152">OUTPUTS</span></span>

### <span data-ttu-id="296d1-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="296d1-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="296d1-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="296d1-154">NOTES</span></span>

## <span data-ttu-id="296d1-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="296d1-155">RELATED LINKS</span></span>

[<span data-ttu-id="296d1-156">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="296d1-156">Get-AzResourceLock</span></span>](./Get-AzResourceLock.md)

[<span data-ttu-id="296d1-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="296d1-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="296d1-158">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="296d1-158">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


