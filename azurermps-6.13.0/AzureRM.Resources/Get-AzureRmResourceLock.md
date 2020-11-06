---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 9681a88a1a4768617383a25122a0224ae264e088
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430048"
---
# <span data-ttu-id="8293c-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="8293c-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="8293c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8293c-102">SYNOPSIS</span></span>
<span data-ttu-id="8293c-103">Obtém um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="8293c-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8293c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8293c-104">SYNTAX</span></span>

### <span data-ttu-id="8293c-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8293c-105">ByResourceGroup</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8293c-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="8293c-106">ByResourceGroupLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8293c-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="8293c-107">BySpecifiedScope</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8293c-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="8293c-108">BySubscription</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8293c-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="8293c-109">BySubscriptionLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8293c-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="8293c-110">ByTenantLevel</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8293c-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="8293c-111">ByLockId</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8293c-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8293c-112">DESCRIPTION</span></span>
<span data-ttu-id="8293c-113">O cmdlet **Get-AzureRmResourceLock** Obtém bloqueios de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8293c-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="8293c-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8293c-114">EXAMPLES</span></span>

### <span data-ttu-id="8293c-115">Exemplo 1: obter um bloqueio</span><span class="sxs-lookup"><span data-stu-id="8293c-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="8293c-116">Esse comando obtém o bloqueio de recurso chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="8293c-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="8293c-117">OS</span><span class="sxs-lookup"><span data-stu-id="8293c-117">PARAMETERS</span></span>

### <span data-ttu-id="8293c-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8293c-118">-ApiVersion</span></span>
<span data-ttu-id="8293c-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="8293c-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8293c-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="8293c-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8293c-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="8293c-121">-AtScope</span></span>
<span data-ttu-id="8293c-122">Indica que esse cmdlet retorna todos os bloqueios no escopo especificado ou acima dele.</span><span class="sxs-lookup"><span data-stu-id="8293c-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="8293c-123">Se você não especificar esse parâmetro, o cmdlet retornará todos os bloqueios em, acima ou abaixo do escopo.</span><span class="sxs-lookup"><span data-stu-id="8293c-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="8293c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8293c-124">-DefaultProfile</span></span>
<span data-ttu-id="8293c-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8293c-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8293c-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="8293c-126">-InformationAction</span></span>
<span data-ttu-id="8293c-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="8293c-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8293c-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8293c-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8293c-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="8293c-129">Continue</span></span>
- <span data-ttu-id="8293c-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="8293c-130">Ignore</span></span>
- <span data-ttu-id="8293c-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="8293c-131">Inquire</span></span>
- <span data-ttu-id="8293c-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8293c-132">SilentlyContinue</span></span>
- <span data-ttu-id="8293c-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="8293c-133">Stop</span></span>
- <span data-ttu-id="8293c-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="8293c-134">Suspend</span></span>

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

### <span data-ttu-id="8293c-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8293c-135">-InformationVariable</span></span>
<span data-ttu-id="8293c-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="8293c-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8293c-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="8293c-137">-LockId</span></span>
<span data-ttu-id="8293c-138">Especifica a ID do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8293c-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8293c-139">-Lockname</span><span class="sxs-lookup"><span data-stu-id="8293c-139">-LockName</span></span>
<span data-ttu-id="8293c-140">Especifica o nome do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="8293c-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8293c-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="8293c-141">-Pre</span></span>
<span data-ttu-id="8293c-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8293c-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8293c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8293c-143">-ResourceGroupName</span></span>
<span data-ttu-id="8293c-144">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="8293c-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="8293c-145">Este cmdlet obtém bloqueios para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8293c-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="8293c-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8293c-146">-ResourceName</span></span>
<span data-ttu-id="8293c-147">Especifica o nome do recurso ao qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="8293c-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="8293c-148">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="8293c-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="8293c-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="8293c-149">-ResourceType</span></span>
<span data-ttu-id="8293c-150">Especifica o tipo de recurso do recurso para o qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="8293c-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="8293c-151">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="8293c-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="8293c-152">-Escopo</span><span class="sxs-lookup"><span data-stu-id="8293c-152">-Scope</span></span>
<span data-ttu-id="8293c-153">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="8293c-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="8293c-154">O cmdlet obtém bloqueios para este escopo.</span><span class="sxs-lookup"><span data-stu-id="8293c-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="8293c-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="8293c-155">-TenantLevel</span></span>
<span data-ttu-id="8293c-156">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="8293c-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="8293c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8293c-157">CommonParameters</span></span>
<span data-ttu-id="8293c-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8293c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8293c-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8293c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8293c-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8293c-160">INPUTS</span></span>

## <span data-ttu-id="8293c-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8293c-161">OUTPUTS</span></span>

## <span data-ttu-id="8293c-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8293c-162">NOTES</span></span>

## <span data-ttu-id="8293c-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8293c-163">RELATED LINKS</span></span>

[<span data-ttu-id="8293c-164">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="8293c-164">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="8293c-165">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="8293c-165">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="8293c-166">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="8293c-166">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


