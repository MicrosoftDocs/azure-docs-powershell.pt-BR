---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 3FBF91B8-8EF9-4E05-AD7E-AEFC6EBBFB8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceLock.md
ms.openlocfilehash: 51fc1b96734d269fda3e09d3a22122b18fe3943a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432575"
---
# <span data-ttu-id="95ade-101">Get-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="95ade-101">Get-AzureRmResourceLock</span></span>

## <span data-ttu-id="95ade-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95ade-102">SYNOPSIS</span></span>
<span data-ttu-id="95ade-103">Obtém um bloqueio de recurso.</span><span class="sxs-lookup"><span data-stu-id="95ade-103">Gets a resource lock.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95ade-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95ade-104">SYNTAX</span></span>

### <span data-ttu-id="95ade-105">Um bloqueio no escopo do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="95ade-105">A lock at the resource group scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95ade-106">Um bloqueio no escopo de recursos do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="95ade-106">A lock at the resource group resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95ade-107">Um bloqueio no escopo especificado.</span><span class="sxs-lookup"><span data-stu-id="95ade-107">A lock at the specified scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95ade-108">Um bloqueio no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="95ade-108">A lock at the subscription scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95ade-109">Um bloqueio no escopo do recurso de assinatura.</span><span class="sxs-lookup"><span data-stu-id="95ade-109">A lock at the subscription resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95ade-110">Um bloqueio no escopo do recurso locatário.</span><span class="sxs-lookup"><span data-stu-id="95ade-110">A lock at the tenant resource scope.</span></span>
```
Get-AzureRmResourceLock [-LockName <String>] [-AtScope] -ResourceName <String> -ResourceType <String>
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95ade-111">Um lock, por ID.</span><span class="sxs-lookup"><span data-stu-id="95ade-111">A lock, by Id.</span></span>
```
Get-AzureRmResourceLock [-AtScope] -LockId <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="95ade-112">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95ade-112">DESCRIPTION</span></span>
<span data-ttu-id="95ade-113">O cmdlet **Get-AzureRmResourceLock** Obtém bloqueios de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="95ade-113">The **Get-AzureRmResourceLock** cmdlet gets Azure resource locks.</span></span>

## <span data-ttu-id="95ade-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95ade-114">EXAMPLES</span></span>

### <span data-ttu-id="95ade-115">Exemplo 1: obter um bloqueio</span><span class="sxs-lookup"><span data-stu-id="95ade-115">Example 1: Get a lock</span></span>
```
PS C:\>Get-AzureRmResourceLock -LockName "ContosoSiteLock" -ResourceName "ContosoSite" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="95ade-116">Esse comando obtém o bloqueio de recurso chamado ContosoSiteLock.</span><span class="sxs-lookup"><span data-stu-id="95ade-116">This command gets the resource lock named ContosoSiteLock.</span></span>

## <span data-ttu-id="95ade-117">OS</span><span class="sxs-lookup"><span data-stu-id="95ade-117">PARAMETERS</span></span>

### <span data-ttu-id="95ade-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="95ade-118">-ApiVersion</span></span>
<span data-ttu-id="95ade-119">Especifica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="95ade-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="95ade-120">Se você não especificar uma versão, esse cmdlet usa a versão mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="95ade-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="95ade-121">-AtScope</span><span class="sxs-lookup"><span data-stu-id="95ade-121">-AtScope</span></span>
<span data-ttu-id="95ade-122">Indica que esse cmdlet retorna todos os bloqueios no escopo especificado ou acima dele.</span><span class="sxs-lookup"><span data-stu-id="95ade-122">Indicates that this cmdlet returns all locks at or above the specified scope.</span></span>
<span data-ttu-id="95ade-123">Se você não especificar esse parâmetro, o cmdlet retornará todos os bloqueios em, acima ou abaixo do escopo.</span><span class="sxs-lookup"><span data-stu-id="95ade-123">If you do not specify this parameter, the cmdlet returns all locks at, above, or below the scope.</span></span>

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

### <span data-ttu-id="95ade-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="95ade-124">-InformationAction</span></span>
<span data-ttu-id="95ade-125">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="95ade-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="95ade-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="95ade-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95ade-127">Contínuo</span><span class="sxs-lookup"><span data-stu-id="95ade-127">Continue</span></span>
- <span data-ttu-id="95ade-128">Ignorar</span><span class="sxs-lookup"><span data-stu-id="95ade-128">Ignore</span></span>
- <span data-ttu-id="95ade-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="95ade-129">Inquire</span></span>
- <span data-ttu-id="95ade-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="95ade-130">SilentlyContinue</span></span>
- <span data-ttu-id="95ade-131">Finaliza</span><span class="sxs-lookup"><span data-stu-id="95ade-131">Stop</span></span>
- <span data-ttu-id="95ade-132">Suspensão</span><span class="sxs-lookup"><span data-stu-id="95ade-132">Suspend</span></span>

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

### <span data-ttu-id="95ade-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="95ade-133">-InformationVariable</span></span>
<span data-ttu-id="95ade-134">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="95ade-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="95ade-135">-LockId</span><span class="sxs-lookup"><span data-stu-id="95ade-135">-LockId</span></span>
<span data-ttu-id="95ade-136">Especifica a ID do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="95ade-136">Specifies the ID of the lock that this cmdlet gets.</span></span>

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

### <span data-ttu-id="95ade-137">-Lockname</span><span class="sxs-lookup"><span data-stu-id="95ade-137">-LockName</span></span>
<span data-ttu-id="95ade-138">Especifica o nome do bloqueio que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="95ade-138">Specifies the name of the lock that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: A lock at the resource group scope., A lock at the resource group resource scope., A lock at the specified scope., A lock at the subscription scope., A lock at the subscription resource scope., A lock at the tenant resource scope.
Aliases: ExtensionResourceName, Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95ade-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="95ade-139">-Pre</span></span>
<span data-ttu-id="95ade-140">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="95ade-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="95ade-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ade-141">-ResourceGroupName</span></span>
<span data-ttu-id="95ade-142">Especifica o nome do grupo de recursos para o qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="95ade-142">Specifies the name of the resource group for which the lock applies.</span></span>
<span data-ttu-id="95ade-143">Este cmdlet obtém bloqueios para este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="95ade-143">This cmdlet gets locks for this resource group.</span></span>

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

### <span data-ttu-id="95ade-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="95ade-144">-ResourceName</span></span>
<span data-ttu-id="95ade-145">Especifica o nome do recurso ao qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="95ade-145">Specifies the name of the resource for which this lock applies.</span></span>
<span data-ttu-id="95ade-146">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="95ade-146">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="95ade-147">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="95ade-147">-ResourceType</span></span>
<span data-ttu-id="95ade-148">Especifica o tipo de recurso do recurso para o qual esse bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="95ade-148">Specifies the resource type of the resource for which this lock applies.</span></span>
<span data-ttu-id="95ade-149">Este cmdlet obtém bloqueios para este recurso.</span><span class="sxs-lookup"><span data-stu-id="95ade-149">This cmdlet gets locks for this resource.</span></span>

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

### <span data-ttu-id="95ade-150">-Escopo</span><span class="sxs-lookup"><span data-stu-id="95ade-150">-Scope</span></span>
<span data-ttu-id="95ade-151">Especifica o escopo ao qual o bloqueio se aplica.</span><span class="sxs-lookup"><span data-stu-id="95ade-151">Specifies the scope to which the lock applies.</span></span>
<span data-ttu-id="95ade-152">O cmdlet obtém bloqueios para este escopo.</span><span class="sxs-lookup"><span data-stu-id="95ade-152">The cmdlet gets locks for this scope.</span></span>

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

### <span data-ttu-id="95ade-153">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="95ade-153">-TenantLevel</span></span>
<span data-ttu-id="95ade-154">Indica que esse cmdlet opera no nível do locatário.</span><span class="sxs-lookup"><span data-stu-id="95ade-154">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="95ade-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ade-155">-DefaultProfile</span></span>
<span data-ttu-id="95ade-156">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95ade-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95ade-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ade-157">CommonParameters</span></span>
<span data-ttu-id="95ade-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95ade-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ade-159">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95ade-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ade-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95ade-160">INPUTS</span></span>

## <span data-ttu-id="95ade-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95ade-161">OUTPUTS</span></span>

### <span data-ttu-id="95ade-162">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="95ade-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="95ade-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95ade-163">NOTES</span></span>

## <span data-ttu-id="95ade-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95ade-164">RELATED LINKS</span></span>

[<span data-ttu-id="95ade-165">New-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="95ade-165">New-AzureRmResourceLock</span></span>](./New-AzureRmResourceLock.md)

[<span data-ttu-id="95ade-166">Remove-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="95ade-166">Remove-AzureRmResourceLock</span></span>](./Remove-AzureRmResourceLock.md)

[<span data-ttu-id="95ade-167">Set-AzureRmResourceLock</span><span class="sxs-lookup"><span data-stu-id="95ade-167">Set-AzureRmResourceLock</span></span>](./Set-AzureRmResourceLock.md)


