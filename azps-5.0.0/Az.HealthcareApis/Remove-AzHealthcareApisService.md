---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 12db158089473c5f0cfb01e24b762ecf192f8991
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117377"
---
# <span data-ttu-id="b6cae-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b6cae-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="b6cae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6cae-102">SYNOPSIS</span></span>
<span data-ttu-id="b6cae-103">Exclui uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="b6cae-103">Deletes a service instance.</span></span>

## <span data-ttu-id="b6cae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6cae-104">SYNTAX</span></span>

### <span data-ttu-id="b6cae-105">ServiceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6cae-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cae-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6cae-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6cae-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6cae-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6cae-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6cae-108">DESCRIPTION</span></span>
<span data-ttu-id="b6cae-109">Exclui uma instância de serviço.</span><span class="sxs-lookup"><span data-stu-id="b6cae-109">Deletes a service instance.</span></span>

## <span data-ttu-id="b6cae-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6cae-110">EXAMPLES</span></span>

### <span data-ttu-id="b6cae-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b6cae-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="b6cae-112">Exclui o serviço HealthcareApis existente com o nome fornecido dentro de um grupo de recursos fornecido.</span><span class="sxs-lookup"><span data-stu-id="b6cae-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="b6cae-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b6cae-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="b6cae-114">Exclui o serviço HealthcareApis existente com o ResourceId fornecido.</span><span class="sxs-lookup"><span data-stu-id="b6cae-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="b6cae-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b6cae-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="b6cae-116">Exclui o objeto de serviço HealthcareApis fornecido.</span><span class="sxs-lookup"><span data-stu-id="b6cae-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="b6cae-117">OS</span><span class="sxs-lookup"><span data-stu-id="b6cae-117">PARAMETERS</span></span>

### <span data-ttu-id="b6cae-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6cae-118">-AsJob</span></span>
<span data-ttu-id="b6cae-119">Executar o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b6cae-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="b6cae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6cae-120">-DefaultProfile</span></span>
<span data-ttu-id="b6cae-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6cae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6cae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6cae-122">-InputObject</span></span>
<span data-ttu-id="b6cae-123">Objeto de serviço HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="b6cae-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="b6cae-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6cae-124">-Name</span></span>
<span data-ttu-id="b6cae-125">Nome do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b6cae-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="b6cae-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6cae-126">-PassThru</span></span>
<span data-ttu-id="b6cae-127">Se fornecido, retorna verdadeiro se a operação foi bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="b6cae-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="b6cae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6cae-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6cae-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6cae-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b6cae-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6cae-130">-ResourceId</span></span>
<span data-ttu-id="b6cae-131">ResourceId do serviço HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b6cae-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="b6cae-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6cae-132">-Confirm</span></span>
<span data-ttu-id="b6cae-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6cae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6cae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6cae-134">-WhatIf</span></span>
<span data-ttu-id="b6cae-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6cae-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6cae-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6cae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6cae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6cae-137">CommonParameters</span></span>
<span data-ttu-id="b6cae-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6cae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6cae-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6cae-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6cae-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6cae-140">INPUTS</span></span>

### <span data-ttu-id="b6cae-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b6cae-141">System.String</span></span>

### <span data-ttu-id="b6cae-142">Microsoft. Azure. Commands. HealthcareApisService. Models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b6cae-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="b6cae-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6cae-143">OUTPUTS</span></span>

### <span data-ttu-id="b6cae-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6cae-144">System.Boolean</span></span>

## <span data-ttu-id="b6cae-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6cae-145">NOTES</span></span>

## <span data-ttu-id="b6cae-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6cae-146">RELATED LINKS</span></span>
