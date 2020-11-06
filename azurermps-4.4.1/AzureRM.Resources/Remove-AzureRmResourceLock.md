---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 42EEAAA8-F13B-486B-82BD-F646EF0DCDBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceLock.md
ms.openlocfilehash: c45d78b815586e54c9f39cfd536fed5a26c2eb19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432555"
---
# <span data-ttu-id="13f0e-101">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="13f0e-101">Remove-AzureRmResourceLock</span></span>

## <span data-ttu-id="13f0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="13f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="13f0e-103">Remove um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="13f0e-103">Removes a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13f0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13f0e-104">SYNTAX</span></span>

### <span data-ttu-id="13f0e-105">Um lock, por ID. (padrão)</span><span class="sxs-lookup"><span data-stu-id="13f0e-105">A lock, by Id. (Default)</span></span>
```
Remove-AzureRmResourceLock [-Force] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f0e-106">Um bloqueio no escopo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13f0e-106">A lock at the resource group scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f0e-107">Um bloqueio no escopo de recursos do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="13f0e-107">A lock at the resource group resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13f0e-108">Um bloqueio no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="13f0e-108">A lock at the specified scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f0e-109">Um bloqueio no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="13f0e-109">A lock at the subscription scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13f0e-110">Um bloqueio no escopo do recurso de assinatura.</span><span class="sxs-lookup"><span data-stu-id="13f0e-110">A lock at the subscription resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13f0e-111">Um bloqueio no escopo do recurso locatário.</span><span class="sxs-lookup"><span data-stu-id="13f0e-111">A lock at the tenant resource scope.</span></span>
```
Remove-AzureRmResourceLock -LockName <String> [-Force] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13f0e-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="13f0e-112">DESCRIPTION</span></span>
<span data-ttu-id="13f0e-113">O cmdlet **Remove-AzureRmResourceLock** remove um bloqueio de recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="13f0e-113">The **Remove-AzureRmResourceLock** cmdlet removes an Azure resource lock.</span></span>

## <span data-ttu-id="13f0e-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13f0e-114">EXAMPLES</span></span>

### <span data-ttu-id="13f0e-115">Exemplo 1: remover um bloqueio</span><span class="sxs-lookup"><span data-stu-id="13f0e-115">Example 1: Remove a lock</span></span>
```
PS C:\>Remove-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Storage-SouthCentralUS/providers/Microsoft.ClassicStorage/storageAccounts/mystorageaccount/providers/Microsoft.Authorization/locks/test"
```

<span data-ttu-id="13f0e-116">Esse comando Remove o bloqueio chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="13f0e-116">This command removes the lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="13f0e-117">OS</span><span class="sxs-lookup"><span data-stu-id="13f0e-117">PARAMETERS</span></span>

### <span data-ttu-id="13f0e-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="13f0e-118">-ApiVersion</span></span>
<span data-ttu-id="13f0e-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="13f0e-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="13f0e-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="13f0e-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="13f0e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="13f0e-121">-Force</span></span>
<span data-ttu-id="13f0e-122">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="13f0e-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13f0e-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="13f0e-123">-InformationAction</span></span>
<span data-ttu-id="13f0e-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="13f0e-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="13f0e-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="13f0e-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="13f0e-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="13f0e-126">Continue</span></span>
- <span data-ttu-id="13f0e-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="13f0e-127">Ignore</span></span>
- <span data-ttu-id="13f0e-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="13f0e-128">Inquire</span></span>
- <span data-ttu-id="13f0e-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="13f0e-129">SilentlyContinue</span></span>
- <span data-ttu-id="13f0e-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="13f0e-130">Stop</span></span>
- <span data-ttu-id="13f0e-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="13f0e-131">Suspend</span></span>

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

### <span data-ttu-id="13f0e-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="13f0e-132">-InformationVariable</span></span>
<span data-ttu-id="13f0e-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="13f0e-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="13f0e-134">-LockId</span><span class="sxs-lookup"><span data-stu-id="13f0e-134">-LockId</span></span>
<span data-ttu-id="13f0e-135">Especifica a ID do bloqueio que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="13f0e-135">Specifies the ID of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock, by Id.
Aliases: Id, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f0e-136">-Lockname</span><span class="sxs-lookup"><span data-stu-id="13f0e-136">-LockName</span></span>
<span data-ttu-id="13f0e-137">Especifica o nome do bloqueio que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="13f0e-137">Specifies the name of the lock that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f0e-138">-Pre</span><span class="sxs-lookup"><span data-stu-id="13f0e-138">-Pre</span></span>
<span data-ttu-id="13f0e-139">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="13f0e-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="13f0e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f0e-140">-ResourceGroupName</span></span>
<span data-ttu-id="13f0e-141">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="13f0e-141">Specifies the name of the resource group for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f0e-142">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="13f0e-142">-ResourceName</span></span>
<span data-ttu-id="13f0e-143">Especifica o nome do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="13f0e-143">Specifies the name of the resource for which the lock applies.</span></span>
<span data-ttu-id="13f0e-144">Por exemplo, para especificar um banco de dados, use o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="13f0e-144">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="13f0e-145">Banco de dados do servidor `/`</span><span class="sxs-lookup"><span data-stu-id="13f0e-145">Server`/`Database</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f0e-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="13f0e-146">-ResourceType</span></span>
<span data-ttu-id="13f0e-147">Especifica o tipo de recurso do recurso para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="13f0e-147">Specifies the resource type of the resource for which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group resource scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f0e-148">-Escopo</span><span class="sxs-lookup"><span data-stu-id="13f0e-148">-Scope</span></span>
<span data-ttu-id="13f0e-149">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="13f0e-149">Specifies the scope to which the lock applies.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the specified scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13f0e-150">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="13f0e-150">-TenantLevel</span></span>
<span data-ttu-id="13f0e-151">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="13f0e-151">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: A lock at the tenant resource scope.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13f0e-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="13f0e-152">-Confirm</span></span>
<span data-ttu-id="13f0e-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13f0e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13f0e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13f0e-154">-WhatIf</span></span>
<span data-ttu-id="13f0e-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="13f0e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13f0e-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="13f0e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13f0e-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f0e-157">-DefaultProfile</span></span>
<span data-ttu-id="13f0e-158">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13f0e-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f0e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f0e-159">CommonParameters</span></span>
<span data-ttu-id="13f0e-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13f0e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f0e-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13f0e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f0e-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="13f0e-162">INPUTS</span></span>

## <span data-ttu-id="13f0e-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="13f0e-163">OUTPUTS</span></span>

### <span data-ttu-id="13f0e-164">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="13f0e-164">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="13f0e-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="13f0e-165">NOTES</span></span>

## <span data-ttu-id="13f0e-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13f0e-166">RELATED LINKS</span></span>

[<span data-ttu-id="13f0e-167">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="13f0e-167">Get-AzureRmResourceLock</span></span>](./Get-AzureRmResourceLock.md)

[<span data-ttu-id="13f0e-168">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="13f0e-168">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="13f0e-169">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="13f0e-169">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


