---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: af406af487e03c429a21a99799083f67d0fabf53
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891396"
---
# <span data-ttu-id="26187-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="26187-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="26187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26187-102">SYNOPSIS</span></span>
<span data-ttu-id="26187-103">Obtém informações sobre Trabalhos de Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="26187-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="26187-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="26187-104">SYNTAX</span></span>

### <span data-ttu-id="26187-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="26187-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26187-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26187-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26187-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26187-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26187-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="26187-108">DESCRIPTION</span></span>
<span data-ttu-id="26187-109">O cmdlet **Get-AzDataBoxJobs** obtém informações sobre trabalhos de caixa de dados em uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="26187-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="26187-110">Se você especificar o Grupo de Recursos, esse cmdlet obtém todos os trabalhos da caixa de dados nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="26187-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="26187-111">Se você especificar o Nome do trabalho juntamente com o nome do grupo de recursos, esse cmdlet obterá informações sobre esse trabalho específico da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="26187-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="26187-112">Se você não especificar nada além da ID da assinatura, este cmdlet obterá informações sobre todos os trabalhos da caixa de dados sob essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="26187-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="26187-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="26187-113">EXAMPLES</span></span>

### <span data-ttu-id="26187-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="26187-114">Example 1</span></span>
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

<span data-ttu-id="26187-115">Get-AzDataBoxJob sem qualquer parâmetro busca todos os trabalhos de caixa de dados sob a assinatura</span><span class="sxs-lookup"><span data-stu-id="26187-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="26187-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="26187-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="26187-117">Get-AzDataBoxJob parâmetro ResourceGroupName busca todos os trabalhos da caixa de dados no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="26187-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="26187-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="26187-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="26187-119">Get-AzDataBoxJob resourceGroupName e Name especificados buscarão esse trabalho específico da caixa de dados</span><span class="sxs-lookup"><span data-stu-id="26187-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="26187-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="26187-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="26187-121">Get-AzDataBoxJob resourceId especificado buscará esse trabalho específico de caixa de dados</span><span class="sxs-lookup"><span data-stu-id="26187-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="26187-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="26187-122">PARAMETERS</span></span>

### <span data-ttu-id="26187-123">-Abortado</span><span class="sxs-lookup"><span data-stu-id="26187-123">-Aborted</span></span>
<span data-ttu-id="26187-124">Parâmetro Switch para buscar trabalhos abortados</span><span class="sxs-lookup"><span data-stu-id="26187-124">Switch Parameter to fetch Aborted jobs</span></span>

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

### <span data-ttu-id="26187-125">-Cancelled</span><span class="sxs-lookup"><span data-stu-id="26187-125">-Cancelled</span></span>
<span data-ttu-id="26187-126">Parâmetro Switch para buscar trabalhos cancelados</span><span class="sxs-lookup"><span data-stu-id="26187-126">Switch Parameter to fetch Cancelled jobs</span></span>

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

### <span data-ttu-id="26187-127">-Completed</span><span class="sxs-lookup"><span data-stu-id="26187-127">-Completed</span></span>
<span data-ttu-id="26187-128">Parâmetro Switch para buscar trabalhos concluídos</span><span class="sxs-lookup"><span data-stu-id="26187-128">Switch Parameter to fetch Completed jobs</span></span>

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

### <span data-ttu-id="26187-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="26187-129">-CompletedWithError</span></span>
<span data-ttu-id="26187-130">Parâmetro Switch para buscar trabalhos concluídos com erros</span><span class="sxs-lookup"><span data-stu-id="26187-130">Switch Parameter to fetch jobs completed with errors</span></span>

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

### <span data-ttu-id="26187-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26187-131">-DefaultProfile</span></span>
<span data-ttu-id="26187-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="26187-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26187-133">-Name</span><span class="sxs-lookup"><span data-stu-id="26187-133">-Name</span></span>
<span data-ttu-id="26187-134">Nome do Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="26187-134">Databox Job Name</span></span>

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

### <span data-ttu-id="26187-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26187-135">-ResourceGroupName</span></span>
<span data-ttu-id="26187-136">Nome do Grupo de Recursos de Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="26187-136">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="26187-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26187-137">-ResourceId</span></span>
<span data-ttu-id="26187-138">ID do Recurso de Trabalho da Caixa de Dados</span><span class="sxs-lookup"><span data-stu-id="26187-138">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="26187-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26187-139">CommonParameters</span></span>
<span data-ttu-id="26187-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26187-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26187-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26187-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26187-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26187-142">INPUTS</span></span>

### <span data-ttu-id="26187-143">System.String</span><span class="sxs-lookup"><span data-stu-id="26187-143">System.String</span></span>

## <span data-ttu-id="26187-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="26187-144">OUTPUTS</span></span>

### <span data-ttu-id="26187-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="26187-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="26187-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="26187-146">NOTES</span></span>

## <span data-ttu-id="26187-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="26187-147">RELATED LINKS</span></span>
