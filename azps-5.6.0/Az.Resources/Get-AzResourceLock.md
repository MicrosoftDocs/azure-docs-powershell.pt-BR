---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcelock
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceLock.md
ms.openlocfilehash: 70c52508bbb152047d40d7556a41ad76e3ca2eac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886858"
---
# <span data-ttu-id="f4f6f-101">Get-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f4f6f-101">Get-AzResourceLock</span></span>

## <span data-ttu-id="f4f6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f6f-103">Obtém um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-103">Gets a resource lock.</span></span>

## <span data-ttu-id="f4f6f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f4f6f-104">SYNTAX</span></span>

### <span data-ttu-id="f4f6f-105">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f4f6f-105">ByResourceGroup</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f6f-106">ByResourceGroupLevel</span><span class="sxs-lookup"><span data-stu-id="f4f6f-106">ByResourceGroupLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4f6f-107">BySpecifiedScope</span><span class="sxs-lookup"><span data-stu-id="f4f6f-107">BySpecifiedScope</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f6f-108">BySubscription</span><span class="sxs-lookup"><span data-stu-id="f4f6f-108">BySubscription</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f6f-109">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f4f6f-109">BySubscriptionLevel</span></span>
```
Get-AzResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f4f6f-110">ByLockId</span><span class="sxs-lookup"><span data-stu-id="f4f6f-110">ByLockId</span></span>
```
Get-AzResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4f6f-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f4f6f-111">DESCRIPTION</span></span>
<span data-ttu-id="f4f6f-112">O cmdlet **Get-AzResourceLock** obtém bloqueios de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-112">The **Get-AzResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="f4f6f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4f6f-113">EXAMPLES</span></span>

### <span data-ttu-id="f4f6f-114">Exemplo 1: Obter um bloqueio</span><span class="sxs-lookup"><span data-stu-id="f4f6f-114">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="f4f6f-115">Este comando obtém o bloqueio de recursos chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-115">This command gets the resource lock named ContosoSiteLock.</span></span>

### <span data-ttu-id="f4f6f-116">Exemplo 2: Obter bloqueios no nível do grupo de recursos ou superior</span><span class="sxs-lookup"><span data-stu-id="f4f6f-116">Example 2: Get locks at resource group level or higher</span></span>
```
PS C:\> Get-AzResourceLock -ResourceGroupName "ResourceGroup11" -AtScope
```

<span data-ttu-id="f4f6f-117">Esse comando obtém os bloqueios de recursos no grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-117">This command gets the resource locks on the resource group or the subscription.</span></span>

## <span data-ttu-id="f4f6f-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f4f6f-118">PARAMETERS</span></span>

### <span data-ttu-id="f4f6f-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f4f6f-119">-ApiVersion</span></span>
<span data-ttu-id="f4f6f-120">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f4f6f-121">Se você não especificar uma versão, este cmdlet usará a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f4f6f-122">-AtScope</span><span class="sxs-lookup"><span data-stu-id="f4f6f-122">-AtScope</span></span>
<span data-ttu-id="f4f6f-123">Indica que esse cmdlet retorna todos os bloqueios em ou acima do escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-123">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="f4f6f-124">Se você não especificar esse parâmetro, o cmdlet retornará todos os bloqueios em, acima ou abaixo do escopo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-124">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="f4f6f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f6f-125">-DefaultProfile</span></span>
<span data-ttu-id="f4f6f-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="f4f6f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4f6f-127">-LockId</span><span class="sxs-lookup"><span data-stu-id="f4f6f-127">-LockId</span></span>
<span data-ttu-id="f4f6f-128">Especifica a ID do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-128">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4f6f-129">-LockName</span><span class="sxs-lookup"><span data-stu-id="f4f6f-129">-LockName</span></span>
<span data-ttu-id="f4f6f-130">Especifica o nome do bloqueio que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-130">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByResourceGroupLevel, BySpecifiedScope, BySubscription, BySubscriptionLevel
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4f6f-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="f4f6f-131">-Pre</span></span>
<span data-ttu-id="f4f6f-132">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f4f6f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f6f-133">-ResourceGroupName</span></span>
<span data-ttu-id="f4f6f-134">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-134">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="f4f6f-135">Este cmdlet obtém bloqueios para esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-135">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="f4f6f-136">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f4f6f-136">-ResourceName</span></span>
<span data-ttu-id="f4f6f-137">Especifica o nome do recurso para o qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-137">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="f4f6f-138">Este cmdlet obtém bloqueios para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-138">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f4f6f-139">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f4f6f-139">-ResourceType</span></span>
<span data-ttu-id="f4f6f-140">Especifica o tipo de recurso do recurso para o qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-140">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="f4f6f-141">Este cmdlet obtém bloqueios para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-141">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="f4f6f-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="f4f6f-142">-Scope</span></span>
<span data-ttu-id="f4f6f-143">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-143">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="f4f6f-144">O cmdlet obtém bloqueios para esse escopo.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-144">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="f4f6f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f6f-145">CommonParameters</span></span>
<span data-ttu-id="f4f6f-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f6f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f6f-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4f6f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f6f-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4f6f-148">INPUTS</span></span>

### <span data-ttu-id="f4f6f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f4f6f-149">System.String</span></span>

## <span data-ttu-id="f4f6f-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f4f6f-150">OUTPUTS</span></span>

### <span data-ttu-id="f4f6f-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f4f6f-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f4f6f-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="f4f6f-152">NOTES</span></span>

## <span data-ttu-id="f4f6f-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4f6f-153">RELATED LINKS</span></span>

[<span data-ttu-id="f4f6f-154">New-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f4f6f-154">New-AzResourceLock</span></span>](./New-AzResourceLock.md)

[<span data-ttu-id="f4f6f-155">Remove-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f4f6f-155">Remove-AzResourceLock</span></span>](./Remove-AzResourceLock.md)

[<span data-ttu-id="f4f6f-156">Set-AzResourceLock</span><span class="sxs-lookup"><span data-stu-id="f4f6f-156">Set-AzResourceLock</span></span>](./Set-AzResourceLock.md)


