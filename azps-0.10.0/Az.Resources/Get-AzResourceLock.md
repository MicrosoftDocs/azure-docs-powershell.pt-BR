---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: e774b333703714246de852d3f72ba704d7122b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776426"
---
# <span data-ttu-id="2de87-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2de87-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="2de87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2de87-102">SYNOPSIS</span></span>
<span data-ttu-id="2de87-103">Obtém um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="2de87-103">Gets a resource lock.</span></span>

## <span data-ttu-id="2de87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2de87-104">SYNTAX</span></span>

### <span data-ttu-id="2de87-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2de87-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2de87-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="2de87-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2de87-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="2de87-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2de87-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="2de87-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2de87-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="2de87-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2de87-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="2de87-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2de87-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="2de87-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2de87-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2de87-112">DESCRIPTION</span></span>
<span data-ttu-id="2de87-113">O cmdlet **Get-AzResourceLock** Obtém bloqueios de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2de87-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="2de87-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2de87-114">EXAMPLES</span></span>

### <span data-ttu-id="2de87-115">Exemplo 1: obter um bloqueio</span><span class="sxs-lookup"><span data-stu-id="2de87-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="2de87-116">Esse comando obtém o bloqueio de recurso chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="2de87-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="2de87-117">OS</span><span class="sxs-lookup"><span data-stu-id="2de87-117">PARAMETERS</span></span>

### <span data-ttu-id="2de87-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2de87-118">-ApiVersion</span></span>
<span data-ttu-id="2de87-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="2de87-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2de87-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="2de87-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2de87-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="2de87-121">-AtScope</span></span>
<span data-ttu-id="2de87-122">Indica que esse cmdlet retorna todos os bloqueios no escopo especificado ou acima dele.</span><span class="sxs-lookup"><span data-stu-id="2de87-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="2de87-123">Se você não especificar esse parâmetro, o cmdlet retornará todos os bloqueios em, acima ou abaixo do escopo.</span><span class="sxs-lookup"><span data-stu-id="2de87-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="2de87-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de87-124">-DefaultProfile</span></span>
<span data-ttu-id="2de87-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2de87-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2de87-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="2de87-126">-InformationAction</span></span>
<span data-ttu-id="2de87-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="2de87-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2de87-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2de87-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2de87-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="2de87-129">Continue</span></span>
- <span data-ttu-id="2de87-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="2de87-130">Ignore</span></span>
- <span data-ttu-id="2de87-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="2de87-131">Inquire</span></span>
- <span data-ttu-id="2de87-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2de87-132">SilentlyContinue</span></span>
- <span data-ttu-id="2de87-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="2de87-133">Stop</span></span>
- <span data-ttu-id="2de87-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="2de87-134">Suspend</span></span>

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

### <span data-ttu-id="2de87-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2de87-135">-InformationVariable</span></span>
<span data-ttu-id="2de87-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="2de87-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2de87-137">-LockId</span><span class="sxs-lookup"><span data-stu-id="2de87-137">-LockId</span></span>
<span data-ttu-id="2de87-138">Especifica a ID do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2de87-138">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2de87-139">-Lockname</span><span class="sxs-lookup"><span data-stu-id="2de87-139">-LockName</span></span>
<span data-ttu-id="2de87-140">Especifica o nome do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="2de87-140">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2de87-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="2de87-141">-Pre</span></span>
<span data-ttu-id="2de87-142">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="2de87-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2de87-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de87-143">-ResourceGroupName</span></span>
<span data-ttu-id="2de87-144">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="2de87-144">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="2de87-145">Este cmdlet obtém bloqueios para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2de87-145">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="2de87-146">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2de87-146">-ResourceName</span></span>
<span data-ttu-id="2de87-147">Especifica o nome do recurso ao qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="2de87-147">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="2de87-148">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="2de87-148">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="2de87-149">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2de87-149">-ResourceType</span></span>
<span data-ttu-id="2de87-150">Especifica o tipo de recurso do recurso para o qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="2de87-150">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="2de87-151">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="2de87-151">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="2de87-152">-Escopo</span><span class="sxs-lookup"><span data-stu-id="2de87-152">-Scope</span></span>
<span data-ttu-id="2de87-153">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="2de87-153">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="2de87-154">O cmdlet obtém bloqueios para este escopo.</span><span class="sxs-lookup"><span data-stu-id="2de87-154">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="2de87-155">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="2de87-155">-TenantLevel</span></span>
<span data-ttu-id="2de87-156">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="2de87-156">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="2de87-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de87-157">CommonParameters</span></span>
<span data-ttu-id="2de87-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de87-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de87-159">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de87-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de87-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2de87-160">INPUTS</span></span>

## <span data-ttu-id="2de87-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2de87-161">OUTPUTS</span></span>

## <span data-ttu-id="2de87-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2de87-162">NOTES</span></span>

## <span data-ttu-id="2de87-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2de87-163">RELATED LINKS</span></span>

[<span data-ttu-id="2de87-164">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2de87-164">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="2de87-165">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2de87-165">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="2de87-166">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="2de87-166">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


