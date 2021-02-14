---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111010"
---
# <span data-ttu-id="c5c00-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c5c00-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="c5c00-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5c00-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c00-103">Obtém informações sobre Trabalhos da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="c5c00-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="c5c00-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5c00-104">SYNTAX</span></span>

### <span data-ttu-id="c5c00-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c5c00-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5c00-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c00-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5c00-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5c00-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5c00-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5c00-108">DESCRIPTION</span></span>
<span data-ttu-id="c5c00-109">O **cmdlet Get-AzDataBoxJobs** obtém informações sobre trabalhos de caixa de dados em uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c5c00-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="c5c00-110">Se você especificar o Grupo de Recursos, esse cmdlet obtém todos os trabalhos da caixa de dados sob esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5c00-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="c5c00-111">Se você especificar o Nome do trabalho juntamente com o nome do grupo de recursos, esse cmdlet obterá informações sobre esse trabalho específico da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="c5c00-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="c5c00-112">Se você não especificar nada além da ID de assinatura, este cmdlet obterá informações sobre todos os trabalhos da caixa de dados nessa assinatura.</span><span class="sxs-lookup"><span data-stu-id="c5c00-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="c5c00-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c5c00-113">EXAMPLES</span></span>

### <span data-ttu-id="c5c00-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5c00-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="c5c00-115">Get-AzDataBoxJob sem parâmetros busca todos os trabalhos da caixa de dados na assinatura</span><span class="sxs-lookup"><span data-stu-id="c5c00-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="c5c00-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c5c00-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="c5c00-117">Get-AzDataBoxJob parâmetro ResourceGroupName busca todos os trabalhos da caixa de dados no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="c5c00-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="c5c00-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c5c00-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="c5c00-119">Get-AzDataBoxJob com ResourceGroupName e Name especificados buscarão esse trabalho específico da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="c5c00-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="c5c00-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c5c00-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="c5c00-121">Get-AzDataBoxJob com ResourceId especificado buscará esse trabalho específico da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="c5c00-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="c5c00-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5c00-122">PARAMETERS</span></span>

### <span data-ttu-id="c5c00-123">-Cancelado</span><span class="sxs-lookup"><span data-stu-id="c5c00-123">-Aborted</span></span>
<span data-ttu-id="c5c00-124">Alternar Parâmetro para buscar trabalhos cancelados</span><span class="sxs-lookup"><span data-stu-id="c5c00-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c00-125">-Cancelado</span><span class="sxs-lookup"><span data-stu-id="c5c00-125">-Cancelled</span></span>
<span data-ttu-id="c5c00-126">Alternar Parâmetro para buscar trabalhos cancelados</span><span class="sxs-lookup"><span data-stu-id="c5c00-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c00-127">-Concluído</span><span class="sxs-lookup"><span data-stu-id="c5c00-127">-Completed</span></span>
<span data-ttu-id="c5c00-128">Alternar Parâmetro para buscar trabalhos concluídos</span><span class="sxs-lookup"><span data-stu-id="c5c00-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c00-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="c5c00-129">-CompletedWithError</span></span>
<span data-ttu-id="c5c00-130">Alternar Parâmetro para buscar trabalhos concluídos com erros</span><span class="sxs-lookup"><span data-stu-id="c5c00-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c00-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5c00-131">-DefaultProfile</span></span>
<span data-ttu-id="c5c00-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5c00-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5c00-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5c00-133">-Name</span></span>
<span data-ttu-id="c5c00-134">Nome do trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="c5c00-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c00-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c00-135">-ResourceGroupName</span></span>
<span data-ttu-id="c5c00-136">Nome do grupo de recursos de trabalho da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="c5c00-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5c00-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c00-137">-ResourceId</span></span>
<span data-ttu-id="c5c00-138">ID do Recurso de Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="c5c00-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5c00-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c00-139">CommonParameters</span></span>
<span data-ttu-id="c5c00-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c00-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c00-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5c00-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c00-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="c5c00-142">INPUTS</span></span>

### <span data-ttu-id="c5c00-143">System.String</span><span class="sxs-lookup"><span data-stu-id="c5c00-143">System.String</span></span>

## <span data-ttu-id="c5c00-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="c5c00-144">OUTPUTS</span></span>

### <span data-ttu-id="c5c00-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="c5c00-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="c5c00-146">Notas</span><span class="sxs-lookup"><span data-stu-id="c5c00-146">NOTES</span></span>

## <span data-ttu-id="c5c00-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5c00-147">RELATED LINKS</span></span>
