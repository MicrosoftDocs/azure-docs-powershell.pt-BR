---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 448b400d4a01924d7ef2ce64acc0f7edf827b827
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893298"
---
# <span data-ttu-id="daf85-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="daf85-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="daf85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daf85-102">SYNOPSIS</span></span>
<span data-ttu-id="daf85-103">Exclui uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="daf85-103">Deletes a service instance.</span></span>

## <span data-ttu-id="daf85-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="daf85-104">SYNTAX</span></span>

### <span data-ttu-id="daf85-105">ServiceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="daf85-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daf85-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="daf85-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daf85-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="daf85-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daf85-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="daf85-108">DESCRIPTION</span></span>
<span data-ttu-id="daf85-109">Exclui uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="daf85-109">Deletes a service instance.</span></span>

## <span data-ttu-id="daf85-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="daf85-110">EXAMPLES</span></span>

### <span data-ttu-id="daf85-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="daf85-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="daf85-112">Exclui o serviço HealthcareApis existente com o nome fornecido em um grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="daf85-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="daf85-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="daf85-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="daf85-114">Exclui o serviço HealthcareApis existente com ResourceId fornecido.</span><span class="sxs-lookup"><span data-stu-id="daf85-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="daf85-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="daf85-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="daf85-116">Exclui o objeto de serviço HealthcareApis fornecido.</span><span class="sxs-lookup"><span data-stu-id="daf85-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="daf85-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="daf85-117">PARAMETERS</span></span>

### <span data-ttu-id="daf85-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="daf85-118">-AsJob</span></span>
<span data-ttu-id="daf85-119">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="daf85-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="daf85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf85-120">-DefaultProfile</span></span>
<span data-ttu-id="daf85-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daf85-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daf85-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="daf85-122">-InputObject</span></span>
<span data-ttu-id="daf85-123">Objeto de serviço HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="daf85-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="daf85-124">-Name</span><span class="sxs-lookup"><span data-stu-id="daf85-124">-Name</span></span>
<span data-ttu-id="daf85-125">Nome do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="daf85-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf85-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="daf85-126">-PassThru</span></span>
<span data-ttu-id="daf85-127">Se fornecido, retorna true se a operação foi bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="daf85-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="daf85-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf85-128">-ResourceGroupName</span></span>
<span data-ttu-id="daf85-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="daf85-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf85-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daf85-130">-ResourceId</span></span>
<span data-ttu-id="daf85-131">HealthcareApis Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="daf85-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="daf85-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="daf85-132">-Confirm</span></span>
<span data-ttu-id="daf85-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daf85-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf85-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf85-134">-WhatIf</span></span>
<span data-ttu-id="daf85-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="daf85-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daf85-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="daf85-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daf85-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf85-137">CommonParameters</span></span>
<span data-ttu-id="daf85-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daf85-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf85-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daf85-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf85-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="daf85-140">INPUTS</span></span>

### <span data-ttu-id="daf85-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="daf85-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="daf85-142">System.String</span><span class="sxs-lookup"><span data-stu-id="daf85-142">System.String</span></span>

## <span data-ttu-id="daf85-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="daf85-143">OUTPUTS</span></span>

### <span data-ttu-id="daf85-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="daf85-144">System.Boolean</span></span>

## <span data-ttu-id="daf85-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="daf85-145">NOTES</span></span>

## <span data-ttu-id="daf85-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daf85-146">RELATED LINKS</span></span>
