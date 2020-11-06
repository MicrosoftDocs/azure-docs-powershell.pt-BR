---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 7c9a9da46da232e6b8a7e81e9b698d2b76513c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599417"
---
# <span data-ttu-id="f3fbd-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f3fbd-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="f3fbd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f3fbd-102">SYNOPSIS</span></span>
<span data-ttu-id="f3fbd-103">Obtém um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-103">Gets a resource lock.</span></span>

## <span data-ttu-id="f3fbd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3fbd-104">SYNTAX</span></span>

### <span data-ttu-id="f3fbd-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f3fbd-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fbd-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f3fbd-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3fbd-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="f3fbd-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fbd-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f3fbd-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fbd-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f3fbd-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fbd-110">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f3fbd-110">ByTenantLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String> [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fbd-111">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f3fbd-111">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3fbd-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f3fbd-112">DESCRIPTION</span></span>
<span data-ttu-id="f3fbd-113">O cmdlet **Get-AzResourceLock** Obtém bloqueios de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-113">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="f3fbd-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3fbd-114">EXAMPLES</span></span>

### <span data-ttu-id="f3fbd-115">Exemplo 1: obter um bloqueio</span><span class="sxs-lookup"><span data-stu-id="f3fbd-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f3fbd-116">Esse comando obtém o bloqueio de recurso chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="f3fbd-117">OS</span><span class="sxs-lookup"><span data-stu-id="f3fbd-117">PARAMETERS</span></span>

### <span data-ttu-id="f3fbd-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f3fbd-118">-ApiVersion</span></span>
<span data-ttu-id="f3fbd-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f3fbd-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f3fbd-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="f3fbd-121">-AtScope</span></span>
<span data-ttu-id="f3fbd-122">Indica que esse cmdlet retorna todos os bloqueios no escopo especificado ou acima dele.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="f3fbd-123">Se você não especificar esse parâmetro, o cmdlet retornará todos os bloqueios em, acima ou abaixo do escopo.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="f3fbd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3fbd-124">-DefaultProfile</span></span>
<span data-ttu-id="f3fbd-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f3fbd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3fbd-126">-LockId</span><span class="sxs-lookup"><span data-stu-id="f3fbd-126">-LockId</span></span>
<span data-ttu-id="f3fbd-127">Especifica a ID do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-127">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f3fbd-128">-Lockname</span><span class="sxs-lookup"><span data-stu-id="f3fbd-128">-LockName</span></span>
<span data-ttu-id="f3fbd-129">Especifica o nome do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-129">Specifies the name of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f3fbd-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="f3fbd-130">-Pre</span></span>
<span data-ttu-id="f3fbd-131">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f3fbd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3fbd-132">-ResourceGroupName</span></span>
<span data-ttu-id="f3fbd-133">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-133">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="f3fbd-134">Este cmdlet obtém bloqueios para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-134">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="f3fbd-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f3fbd-135">-ResourceName</span></span>
<span data-ttu-id="f3fbd-136">Especifica o nome do recurso ao qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-136">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="f3fbd-137">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-137">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f3fbd-138">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f3fbd-138">-ResourceType</span></span>
<span data-ttu-id="f3fbd-139">Especifica o tipo de recurso do recurso para o qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-139">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="f3fbd-140">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-140">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f3fbd-141">-Escopo</span><span class="sxs-lookup"><span data-stu-id="f3fbd-141">-Scope</span></span>
<span data-ttu-id="f3fbd-142">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-142">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f3fbd-143">O cmdlet obtém bloqueios para este escopo.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-143">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="f3fbd-144">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f3fbd-144">-TenantLevel</span></span>
<span data-ttu-id="f3fbd-145">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-145">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="f3fbd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3fbd-146">CommonParameters</span></span>
<span data-ttu-id="f3fbd-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3fbd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3fbd-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3fbd-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3fbd-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f3fbd-149">INPUTS</span></span>

### <span data-ttu-id="f3fbd-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f3fbd-150">System.String</span></span>

## <span data-ttu-id="f3fbd-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f3fbd-151">OUTPUTS</span></span>

### <span data-ttu-id="f3fbd-152">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="f3fbd-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f3fbd-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f3fbd-153">NOTES</span></span>

## <span data-ttu-id="f3fbd-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3fbd-154">RELATED LINKS</span></span>

[<span data-ttu-id="f3fbd-155">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f3fbd-155">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="f3fbd-156">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f3fbd-156">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="f3fbd-157">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f3fbd-157">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


