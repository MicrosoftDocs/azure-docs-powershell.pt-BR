---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/get-azimagebuilderrunoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Get-AzImageBuilderRunOutput.md
ms.openlocfilehash: 4cc45f3b4cd21e41f1b2e410dd2b76b9571a4431
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258887"
---
# <span data-ttu-id="ba054-101">Get-AzImageBuilderRunOutput</span><span class="sxs-lookup"><span data-stu-id="ba054-101">Get-AzImageBuilderRunOutput</span></span>

## <span data-ttu-id="ba054-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba054-102">SYNOPSIS</span></span>
<span data-ttu-id="ba054-103">Obter a saída de execução especificada para o recurso de modelo de imagem especificado</span><span class="sxs-lookup"><span data-stu-id="ba054-103">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="ba054-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba054-104">SYNTAX</span></span>

### <span data-ttu-id="ba054-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="ba054-105">List (Default)</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba054-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ba054-106">Get</span></span>
```
Get-AzImageBuilderRunOutput -ImageTemplateName <String> -ResourceGroupName <String> -RunOutputName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ba054-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ba054-107">GetViaIdentity</span></span>
```
Get-AzImageBuilderRunOutput -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba054-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba054-108">DESCRIPTION</span></span>
<span data-ttu-id="ba054-109">Obter a saída de execução especificada para o recurso de modelo de imagem especificado</span><span class="sxs-lookup"><span data-stu-id="ba054-109">Get the specified run output for the specified image template resource</span></span>

## <span data-ttu-id="ba054-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba054-110">EXAMPLES</span></span>

### <span data-ttu-id="ba054-111">Exemplo 1: listar todos os resultados da execução em um modelo</span><span class="sxs-lookup"><span data-stu-id="ba054-111">Example 1: List all run results under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName lucas-imagetemplate -ResourceGroupName wyunchi-imagebuilder

Name          Type
----          ----
image_lucas_1 Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="ba054-112">Esse comando lista todos os resultados da execução em um modelo.</span><span class="sxs-lookup"><span data-stu-id="ba054-112">This command lists all run results under a template.</span></span>

### <span data-ttu-id="ba054-113">Exemplo 2: obter um resultado de execução em um modelo</span><span class="sxs-lookup"><span data-stu-id="ba054-113">Example 2: Get a run result under a template</span></span>
```powershell
PS C:\> Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx 

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="ba054-114">Esse comando obtém um resultado de execução em um modelo.</span><span class="sxs-lookup"><span data-stu-id="ba054-114">This command gets a run result under a template.</span></span>

### <span data-ttu-id="ba054-115">Exemplo 3: obter um resultado de execução em um modelo</span><span class="sxs-lookup"><span data-stu-id="ba054-115">Example 3: Get a run result under a template</span></span>
```powershell
PS C:\> $result = Get-AzImageBuilderRunOutput -ImageTemplateName template-name-u7gjqx -ResourceGroupName wyunchi-imagebuilder -RunOutputName runout-template-name-u7gjqx
PS C:\> Get-AzImageBuilderRunOutput -InputObject $result

Name                        Type
----                        ----
runout-template-name-u7gjqx Microsoft.VirtualMachineImages/imageTemplates/runOutputs
```

<span data-ttu-id="ba054-116">Esse comando obtém um resultado de execução em um modelo.</span><span class="sxs-lookup"><span data-stu-id="ba054-116">This command gets a run result under a template.</span></span>

## <span data-ttu-id="ba054-117">OS</span><span class="sxs-lookup"><span data-stu-id="ba054-117">PARAMETERS</span></span>

### <span data-ttu-id="ba054-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba054-118">-DefaultProfile</span></span>
<span data-ttu-id="ba054-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ba054-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba054-120">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="ba054-120">-ImageTemplateName</span></span>
<span data-ttu-id="ba054-121">O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="ba054-121">The name of the image Template</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba054-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba054-122">-InputObject</span></span>
<span data-ttu-id="ba054-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ba054-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba054-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba054-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba054-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba054-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba054-126">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="ba054-126">-RunOutputName</span></span>
<span data-ttu-id="ba054-127">O nome da saída de execução</span><span class="sxs-lookup"><span data-stu-id="ba054-127">The name of the run output</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba054-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ba054-128">-SubscriptionId</span></span>
<span data-ttu-id="ba054-129">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba054-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ba054-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ba054-130">The subscription Id forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba054-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba054-131">CommonParameters</span></span>
<span data-ttu-id="ba054-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba054-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba054-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba054-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba054-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba054-134">INPUTS</span></span>

### <span data-ttu-id="ba054-135">Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. IImageBuilderIdentity</span><span class="sxs-lookup"><span data-stu-id="ba054-135">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity</span></span>

## <span data-ttu-id="ba054-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba054-136">OUTPUTS</span></span>

### <span data-ttu-id="ba054-137">Microsoft. Azure. PowerShell. cmdlets. ImageBuilder. Models. Api20200214. IRunOutput</span><span class="sxs-lookup"><span data-stu-id="ba054-137">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IRunOutput</span></span>

## <span data-ttu-id="ba054-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba054-138">NOTES</span></span>

<span data-ttu-id="ba054-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ba054-139">ALIASES</span></span>

<span data-ttu-id="ba054-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="ba054-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ba054-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ba054-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ba054-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ba054-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ba054-143">INPUTobject <IImageBuilderIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ba054-143">INPUTOBJECT <IImageBuilderIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ba054-144">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ba054-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ba054-145">`[ImageTemplateName <String>]`: O nome do modelo de imagem</span><span class="sxs-lookup"><span data-stu-id="ba054-145">`[ImageTemplateName <String>]`: The name of the image Template</span></span>
  - <span data-ttu-id="ba054-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba054-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="ba054-147">`[RunOutputName <String>]`: O nome da saída de execução</span><span class="sxs-lookup"><span data-stu-id="ba054-147">`[RunOutputName <String>]`: The name of the run output</span></span>
  - <span data-ttu-id="ba054-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ba054-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ba054-149">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ba054-149">The subscription Id forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ba054-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba054-150">RELATED LINKS</span></span>

