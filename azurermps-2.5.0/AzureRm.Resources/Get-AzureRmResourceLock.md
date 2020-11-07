---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
ms.openlocfilehash: 81e7ab170dc43af0cf712fd9be3e831f33f7fd97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785849"
---
# <span data-ttu-id="e385d-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e385d-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="e385d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e385d-102">SYNOPSIS</span></span>
<span data-ttu-id="e385d-103">Obtém um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="e385d-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e385d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e385d-104">SYNTAX</span></span>

### <span data-ttu-id="e385d-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e385d-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e385d-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="e385d-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e385d-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="e385d-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e385d-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="e385d-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e385d-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e385d-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e385d-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e385d-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e385d-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="e385d-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e385d-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e385d-112">DESCRIPTION</span></span>
<span data-ttu-id="e385d-113">O cmdlet **Get-AzureRmResourceLock** Obtém bloqueios de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="e385d-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="e385d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e385d-114">EXAMPLES</span></span>

### <span data-ttu-id="e385d-115">Exemplo 1: obter um bloqueio</span><span class="sxs-lookup"><span data-stu-id="e385d-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="e385d-116">Esse comando obtém o bloqueio de recurso chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="e385d-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="e385d-117">OS</span><span class="sxs-lookup"><span data-stu-id="e385d-117">PARAMETERS</span></span>

### <span data-ttu-id="e385d-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e385d-118">-ApiVersion</span></span>
<span data-ttu-id="e385d-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e385d-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e385d-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e385d-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e385d-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="e385d-121">-AtScope</span></span>
<span data-ttu-id="e385d-122">Indica que esse cmdlet retorna todos os bloqueios no escopo especificado ou acima dele.</span><span class="sxs-lookup"><span data-stu-id="e385d-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="e385d-123">Se você não especificar esse parâmetro, o cmdlet retornará todos os bloqueios em, acima ou abaixo do escopo.</span><span class="sxs-lookup"><span data-stu-id="e385d-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="e385d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e385d-124">-DefaultProfile</span></span>
<span data-ttu-id="e385d-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e385d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e385d-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="e385d-126">-InformationAction</span></span>
<span data-ttu-id="e385d-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="e385d-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="e385d-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e385d-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e385d-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="e385d-129">Continue</span></span>
- <span data-ttu-id="e385d-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="e385d-130">Ignore</span></span>
- <span data-ttu-id="e385d-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="e385d-131">Inquire</span></span>
- <span data-ttu-id="e385d-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e385d-132">SilentlyContinue</span></span>
- <span data-ttu-id="e385d-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="e385d-133">Stop</span></span>
- <span data-ttu-id="e385d-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="e385d-134">Suspend</span></span>

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

### <span data-ttu-id="e385d-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e385d-135">-InformationVariable</span></span>
<span data-ttu-id="e385d-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="e385d-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e385d-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="e385d-137">-LockId</span></span>
<span data-ttu-id="e385d-138">Especifica a ID do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e385d-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e385d-139">-Lockname</span><span class="sxs-lookup"><span data-stu-id="e385d-139">-LockName</span></span>
<span data-ttu-id="e385d-140">Especifica o nome do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e385d-140">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel, ByTenantLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e385d-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="e385d-141">-Pre</span></span>
<span data-ttu-id="e385d-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e385d-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e385d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e385d-143">-ResourceGroupName</span></span>
<span data-ttu-id="e385d-144">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="e385d-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="e385d-145">Este cmdlet obtém bloqueios para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e385d-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="e385d-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e385d-146">-ResourceName</span></span>
<span data-ttu-id="e385d-147">Especifica o nome do recurso ao qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="e385d-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="e385d-148">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="e385d-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="e385d-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e385d-149">-ResourceType</span></span>
<span data-ttu-id="e385d-150">Especifica o tipo de recurso do recurso para o qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="e385d-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="e385d-151">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="e385d-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="e385d-152">-Escopo</span><span class="sxs-lookup"><span data-stu-id="e385d-152">-Scope</span></span>
<span data-ttu-id="e385d-153">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="e385d-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="e385d-154">O cmdlet obtém bloqueios para este escopo.</span><span class="sxs-lookup"><span data-stu-id="e385d-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="e385d-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e385d-155">-TenantLevel</span></span>
<span data-ttu-id="e385d-156">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="e385d-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e385d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e385d-157">CommonParameters</span></span>
<span data-ttu-id="e385d-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e385d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e385d-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e385d-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e385d-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e385d-160">INPUTS</span></span>

## <span data-ttu-id="e385d-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e385d-161">OUTPUTS</span></span>

## <span data-ttu-id="e385d-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e385d-162">NOTES</span></span>

## <span data-ttu-id="e385d-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e385d-163">RELATED LINKS</span></span>

[<span data-ttu-id="e385d-164">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e385d-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="e385d-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e385d-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="e385d-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="e385d-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


