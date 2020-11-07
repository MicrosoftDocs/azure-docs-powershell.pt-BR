---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: fdf60c029f260d30aae8983165cbfb4d20203824
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785846"
---
# <span data-ttu-id="e425a-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e425a-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="e425a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e425a-102">SYNOPSIS</span></span>
<span data-ttu-id="e425a-103">Remove um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="e425a-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e425a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e425a-104">SYNTAX</span></span>

### <span data-ttu-id="e425a-105">ByLockId (padrão)</span><span class="sxs-lookup"><span data-stu-id="e425a-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e425a-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e425a-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e425a-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="e425a-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e425a-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="e425a-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e425a-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e425a-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e425a-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e425a-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e425a-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e425a-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e425a-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e425a-112">DESCRIPTION</span></span>
<span data-ttu-id="e425a-113">O cmdlet **Remove-AzureRmResourceLock** remove um bloqueio de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="e425a-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="e425a-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e425a-114">EXAMPLES</span></span>

### <span data-ttu-id="e425a-115">Exemplo 1: remover um bloqueio</span><span class="sxs-lookup"><span data-stu-id="e425a-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="e425a-116">Esse comando Remove o bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="e425a-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="e425a-117">OS</span><span class="sxs-lookup"><span data-stu-id="e425a-117">PARAMETERS</span></span>

### <span data-ttu-id="e425a-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e425a-118">-ApiVersion</span></span>
<span data-ttu-id="e425a-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e425a-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e425a-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e425a-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e425a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e425a-121">-DefaultProfile</span></span>
<span data-ttu-id="e425a-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e425a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e425a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e425a-123">-Force</span></span>
<span data-ttu-id="e425a-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e425a-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e425a-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e425a-125">-InformationAction</span></span>
<span data-ttu-id="e425a-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e425a-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="e425a-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e425a-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e425a-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e425a-128">Continue</span></span>
- <span data-ttu-id="e425a-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e425a-129">Ignore</span></span>
- <span data-ttu-id="e425a-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="e425a-130">Inquire</span></span>
- <span data-ttu-id="e425a-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e425a-131">SilentlyContinue</span></span>
- <span data-ttu-id="e425a-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e425a-132">Stop</span></span>
- <span data-ttu-id="e425a-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e425a-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e425a-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e425a-134">-InformationVariable</span></span>
<span data-ttu-id="e425a-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e425a-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e425a-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="e425a-136">-LockId</span></span>
<span data-ttu-id="e425a-137">Especifica a ID do bloqueio que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e425a-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e425a-138">-Lockname</span><span class="sxs-lookup"><span data-stu-id="e425a-138">-LockName</span></span>
<span data-ttu-id="e425a-139">Especifica o nome do bloqueio que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="e425a-139">Specifies the name of the lock that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e425a-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="e425a-140">-Pre</span></span>
<span data-ttu-id="e425a-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e425a-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e425a-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e425a-142">-ResourceGroupName</span></span>
<span data-ttu-id="e425a-143">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="e425a-143">Specifies the name of the resource group for which the lock applies.</span></span>

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

### <span data-ttu-id="e425a-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e425a-144">-ResourceName</span></span>
<span data-ttu-id="e425a-145">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="e425a-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="e425a-146">Por exemplo, para especificar um banco de dados, use o seguinte formato: banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="e425a-146">For instance, to specify a database, use the following format: Server`/`Database</span></span>

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

### <span data-ttu-id="e425a-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e425a-147">-ResourceType</span></span>
<span data-ttu-id="e425a-148">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="e425a-148">Specifies the resource type of the resource for which the lock applies.</span></span>

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

### <span data-ttu-id="e425a-149">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e425a-149">-Scope</span></span>
<span data-ttu-id="e425a-150">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="e425a-150">Specifies the scope to which the lock applies.</span></span>

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

### <span data-ttu-id="e425a-151">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e425a-151">-TenantLevel</span></span>
<span data-ttu-id="e425a-152">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="e425a-152">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e425a-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e425a-153">-Confirm</span></span>
<span data-ttu-id="e425a-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e425a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e425a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e425a-155">-WhatIf</span></span>
<span data-ttu-id="e425a-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e425a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e425a-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e425a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e425a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e425a-158">CommonParameters</span></span>
<span data-ttu-id="e425a-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e425a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e425a-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e425a-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e425a-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e425a-161">INPUTS</span></span>

## <span data-ttu-id="e425a-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e425a-162">OUTPUTS</span></span>

## <span data-ttu-id="e425a-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e425a-163">NOTES</span></span>

## <span data-ttu-id="e425a-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e425a-164">RELATED LINKS</span></span>

[<span data-ttu-id="e425a-165">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e425a-165">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="e425a-166">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e425a-166">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="e425a-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e425a-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


