---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: ea0ee8e46c70e6dd61e352ce0e7bd5da391c0c66
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777811"
---
# <span data-ttu-id="025af-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="025af-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="025af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="025af-102">SYNOPSIS</span></span>
<span data-ttu-id="025af-103">Obtém um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="025af-103">Gets a resource lock.</span></span>

## <span data-ttu-id="025af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="025af-104">SYNTAX</span></span>

### <span data-ttu-id="025af-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="025af-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="025af-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="025af-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="025af-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="025af-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="025af-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="025af-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="025af-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="025af-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="025af-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="025af-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="025af-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="025af-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="025af-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="025af-112">DESCRIPTION</span></span>
<span data-ttu-id="025af-113">O cmdlet **Get-AzResourceLock** Obtém bloqueios de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="025af-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="025af-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="025af-114">EXAMPLES</span></span>

### <span data-ttu-id="025af-115">Exemplo 1: obter um bloqueio</span><span class="sxs-lookup"><span data-stu-id="025af-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="025af-116">Esse comando obtém o bloqueio de recurso chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="025af-116">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="025af-117">Exemplo 2: obter bloqueios em nível de grupo de recursos ou mais</span><span class="sxs-lookup"><span data-stu-id="025af-117">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="025af-118">Este comando obtém os bloqueios de recursos no grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="025af-118">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="025af-119">OS</span><span class="sxs-lookup"><span data-stu-id="025af-119">PARAMETERS</span></span>

### <span data-ttu-id="025af-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="025af-120">-ApiVersion</span></span>
<span data-ttu-id="025af-121">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="025af-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="025af-122">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="025af-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="025af-123">-AtScope</span><span class="sxs-lookup"><span data-stu-id="025af-123">-AtScope</span></span>
<span data-ttu-id="025af-124">Indica que esse cmdlet retorna todos os bloqueios no escopo especificado ou acima dele.</span><span class="sxs-lookup"><span data-stu-id="025af-124">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="025af-125">Se você não especificar esse parâmetro, o cmdlet retornará todos os bloqueios em, acima ou abaixo do escopo.</span><span class="sxs-lookup"><span data-stu-id="025af-125">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="025af-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025af-126">-DefaultProfile</span></span>
<span data-ttu-id="025af-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="025af-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="025af-128">-LockId</span><span class="sxs-lookup"><span data-stu-id="025af-128">-LockId</span></span>
<span data-ttu-id="025af-129">Especifica a ID do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="025af-129">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="025af-130">-Lockname</span><span class="sxs-lookup"><span data-stu-id="025af-130">-LockName</span></span>
<span data-ttu-id="025af-131">Especifica o nome do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="025af-131">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="025af-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="025af-132">-Pre</span></span>
<span data-ttu-id="025af-133">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="025af-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="025af-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025af-134">-ResourceGroupName</span></span>
<span data-ttu-id="025af-135">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="025af-135">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="025af-136">Este cmdlet obtém bloqueios para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="025af-136">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="025af-137">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="025af-137">-ResourceName</span></span>
<span data-ttu-id="025af-138">Especifica o nome do recurso ao qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="025af-138">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="025af-139">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="025af-139">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="025af-140">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="025af-140">-ResourceType</span></span>
<span data-ttu-id="025af-141">Especifica o tipo de recurso do recurso para o qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="025af-141">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="025af-142">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="025af-142">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="025af-143">-Escopo</span><span class="sxs-lookup"><span data-stu-id="025af-143">-Scope</span></span>
<span data-ttu-id="025af-144">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="025af-144">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="025af-145">O cmdlet obtém bloqueios para este escopo.</span><span class="sxs-lookup"><span data-stu-id="025af-145">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="025af-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="025af-146">-TenantLevel</span></span>
<span data-ttu-id="025af-147">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="025af-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="025af-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025af-148">CommonParameters</span></span>
<span data-ttu-id="025af-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025af-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025af-150">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="025af-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025af-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="025af-151">INPUTS</span></span>

### <span data-ttu-id="025af-152">System. String</span><span class="sxs-lookup"><span data-stu-id="025af-152">System.String</span></span>

## <span data-ttu-id="025af-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="025af-153">OUTPUTS</span></span>

### <span data-ttu-id="025af-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="025af-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="025af-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="025af-155">NOTES</span></span>

## <span data-ttu-id="025af-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="025af-156">RELATED LINKS</span></span>

[<span data-ttu-id="025af-157">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="025af-157">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="025af-158">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="025af-158">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="025af-159">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="025af-159">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


