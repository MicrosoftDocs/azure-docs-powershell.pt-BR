---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: f3034d7197a26e8dd2ba803f478b6a71c8d50e8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602842"
---
# <span data-ttu-id="bfac3-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bfac3-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="bfac3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bfac3-102">SYNOPSIS</span></span>
<span data-ttu-id="bfac3-103">Remove um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="bfac3-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfac3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bfac3-104">SYNTAX</span></span>

### <span data-ttu-id="bfac3-105">ByLockId (padrão)</span><span class="sxs-lookup"><span data-stu-id="bfac3-105">ByLockId (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfac3-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bfac3-106">ByResourceGroup</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfac3-107">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="bfac3-107">ByResourceGroupLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfac3-108">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="bfac3-108">BySpecifiedScope</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfac3-109">BySubscription</span><span class="sxs-lookup"><span data-stu-id="bfac3-109">BySubscription</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfac3-110">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bfac3-110">BySubscriptionLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bfac3-111">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="bfac3-111">ByTenantLevel</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfac3-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bfac3-112">DESCRIPTION</span></span>
<span data-ttu-id="bfac3-113">O cmdlet **Remove-AzureRmResourceLock** remove um bloqueio de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="bfac3-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="bfac3-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bfac3-114">EXAMPLES</span></span>

### <span data-ttu-id="bfac3-115">Exemplo 1: remover um bloqueio</span><span class="sxs-lookup"><span data-stu-id="bfac3-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="bfac3-116">Esse comando Remove o bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="bfac3-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="bfac3-117">OS</span><span class="sxs-lookup"><span data-stu-id="bfac3-117">PARAMETERS</span></span>

### <span data-ttu-id="bfac3-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bfac3-118">-ApiVersion</span></span>
<span data-ttu-id="bfac3-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="bfac3-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bfac3-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="bfac3-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfac3-121">-DefaultProfile</span></span>
<span data-ttu-id="bfac3-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="bfac3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfac3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bfac3-123">-Force</span></span>
<span data-ttu-id="bfac3-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bfac3-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bfac3-125">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="bfac3-125">-InformationAction</span></span>
<span data-ttu-id="bfac3-126">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="bfac3-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bfac3-127">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="bfac3-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bfac3-128">Contínuo</span><span class="sxs-lookup"><span data-stu-id="bfac3-128">Continue</span></span>
- <span data-ttu-id="bfac3-129">Ignorar</span><span class="sxs-lookup"><span data-stu-id="bfac3-129">Ignore</span></span>
- <span data-ttu-id="bfac3-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="bfac3-130">Inquire</span></span>
- <span data-ttu-id="bfac3-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bfac3-131">SilentlyContinue</span></span>
- <span data-ttu-id="bfac3-132">Finaliza</span><span class="sxs-lookup"><span data-stu-id="bfac3-132">Stop</span></span>
- <span data-ttu-id="bfac3-133">Suspensão</span><span class="sxs-lookup"><span data-stu-id="bfac3-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bfac3-134">-InformationVariable</span></span>
<span data-ttu-id="bfac3-135">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="bfac3-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-136">-LockId</span><span class="sxs-lookup"><span data-stu-id="bfac3-136">-LockId</span></span>
<span data-ttu-id="bfac3-137">Especifica a ID do bloqueio que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bfac3-137">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByLockId
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-138">-Lockname</span><span class="sxs-lookup"><span data-stu-id="bfac3-138">-LockName</span></span>
<span data-ttu-id="bfac3-139">Especifica o nome do bloqueio que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="bfac3-139">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="bfac3-140">-Pre</span></span>
<span data-ttu-id="bfac3-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="bfac3-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bfac3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfac3-142">-ResourceGroupName</span></span>
<span data-ttu-id="bfac3-143">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="bfac3-143">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bfac3-144">-ResourceName</span></span>
<span data-ttu-id="bfac3-145">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="bfac3-145">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="bfac3-146">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="bfac3-146">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="bfac3-147">Banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="bfac3-147">Server`/`Database</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bfac3-148">-ResourceType</span></span>
<span data-ttu-id="bfac3-149">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="bfac3-149">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupLevel, BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-150">-Escopo</span><span class="sxs-lookup"><span data-stu-id="bfac3-150">-Scope</span></span>
<span data-ttu-id="bfac3-151">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="bfac3-151">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: String
Parameter Sets: BySpecifiedScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-152">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="bfac3-152">-TenantLevel</span></span>
<span data-ttu-id="bfac3-153">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="bfac3-153">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfac3-154">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bfac3-154">-Confirm</span></span>
<span data-ttu-id="bfac3-155">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfac3-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfac3-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfac3-156">-WhatIf</span></span>
<span data-ttu-id="bfac3-157">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bfac3-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfac3-158">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bfac3-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfac3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfac3-159">CommonParameters</span></span>
<span data-ttu-id="bfac3-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfac3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfac3-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfac3-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfac3-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bfac3-162">INPUTS</span></span>

### <span data-ttu-id="bfac3-163">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="bfac3-163">None</span></span>
<span data-ttu-id="bfac3-164">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="bfac3-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfac3-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bfac3-165">OUTPUTS</span></span>

### <span data-ttu-id="bfac3-166">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="bfac3-166">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bfac3-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bfac3-167">NOTES</span></span>

## <span data-ttu-id="bfac3-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bfac3-168">RELATED LINKS</span></span>

[<span data-ttu-id="bfac3-169">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bfac3-169">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="bfac3-170">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bfac3-170">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="bfac3-171">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="bfac3-171">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


