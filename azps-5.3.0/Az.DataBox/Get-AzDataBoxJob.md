---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 8669ee676f3f2be1f1a0064ed9fbbe88f3d113ee
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429972"
---
# <span data-ttu-id="fb4e2-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="fb4e2-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="fb4e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4e2-103">Obtém informações sobre trabalhos do Databox</span><span class="sxs-lookup"><span data-stu-id="fb4e2-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="fb4e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb4e2-104">SYNTAX</span></span>

### <span data-ttu-id="fb4e2-105">ListParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb4e2-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb4e2-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb4e2-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb4e2-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb4e2-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb4e2-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb4e2-108">DESCRIPTION</span></span>
<span data-ttu-id="fb4e2-109">O cmdlet **Get-AzDataBoxJobs** Obtém informações sobre trabalhos do databox em uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="fb4e2-110">Se você especificar o grupo de recursos, esse cmdlet obterá todos os trabalhos do databox sob esse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="fb4e2-111">Se você especificar o nome do trabalho juntamente com o nome do grupo de recursos, esse cmdlet obterá informações sobre esse trabalho databox específico.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="fb4e2-112">Se você não especificar nada além da ID da assinatura, esse cmdlet obterá informações sobre todos os trabalhos databoxdos sob essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="fb4e2-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb4e2-113">EXAMPLES</span></span>

### <span data-ttu-id="fb4e2-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb4e2-114">Example 1</span></span>
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

<span data-ttu-id="fb4e2-115">Get-AzDataBoxJob sem parâmetros busca todos os trabalhos do databox na assinatura</span><span class="sxs-lookup"><span data-stu-id="fb4e2-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="fb4e2-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="fb4e2-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="fb4e2-117">Get-AzDataBoxJob com o parâmetro ResourceGroupName busca todos os trabalhos databox sob o grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="fb4e2-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="fb4e2-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="fb4e2-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="fb4e2-119">Get-AzDataBoxJob com ResourceGroupName e o nome especificado buscará esse trabalho databox específico</span><span class="sxs-lookup"><span data-stu-id="fb4e2-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="fb4e2-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="fb4e2-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="fb4e2-121">Get-AzDataBoxJob com ResourceId especificado buscará aquele trabalho específico do databox</span><span class="sxs-lookup"><span data-stu-id="fb4e2-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="fb4e2-122">OS</span><span class="sxs-lookup"><span data-stu-id="fb4e2-122">PARAMETERS</span></span>

### <span data-ttu-id="fb4e2-123">-Abortado</span><span class="sxs-lookup"><span data-stu-id="fb4e2-123">-Aborted</span></span>
<span data-ttu-id="fb4e2-124">Parâmetro de alternância para buscar trabalhos abortados</span><span class="sxs-lookup"><span data-stu-id="fb4e2-124">Switch Parameter to fetch Aborted jobs</span></span>

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

### <span data-ttu-id="fb4e2-125">-Cancelado</span><span class="sxs-lookup"><span data-stu-id="fb4e2-125">-Cancelled</span></span>
<span data-ttu-id="fb4e2-126">Parâmetro de alternância para buscar trabalhos cancelados</span><span class="sxs-lookup"><span data-stu-id="fb4e2-126">Switch Parameter to fetch Cancelled jobs</span></span>

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

### <span data-ttu-id="fb4e2-127">-Concluído</span><span class="sxs-lookup"><span data-stu-id="fb4e2-127">-Completed</span></span>
<span data-ttu-id="fb4e2-128">Parâmetro de alternância para buscar trabalhos concluídos</span><span class="sxs-lookup"><span data-stu-id="fb4e2-128">Switch Parameter to fetch Completed jobs</span></span>

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

### <span data-ttu-id="fb4e2-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="fb4e2-129">-CompletedWithError</span></span>
<span data-ttu-id="fb4e2-130">Parâmetro de mudança para busca de trabalhos concluída com erros</span><span class="sxs-lookup"><span data-stu-id="fb4e2-130">Switch Parameter to fetch jobs completed with errors</span></span>

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

### <span data-ttu-id="fb4e2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4e2-131">-DefaultProfile</span></span>
<span data-ttu-id="fb4e2-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb4e2-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb4e2-133">-Name</span></span>
<span data-ttu-id="fb4e2-134">Nome do trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="fb4e2-134">Databox Job Name</span></span>

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

### <span data-ttu-id="fb4e2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4e2-135">-ResourceGroupName</span></span>
<span data-ttu-id="fb4e2-136">Nome do grupo de recursos de trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="fb4e2-136">Databox Job Resource Group Name</span></span>

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

### <span data-ttu-id="fb4e2-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb4e2-137">-ResourceId</span></span>
<span data-ttu-id="fb4e2-138">ID do recurso do trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="fb4e2-138">Databox Job Resource Id</span></span>

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

### <span data-ttu-id="fb4e2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4e2-139">CommonParameters</span></span>
<span data-ttu-id="fb4e2-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4e2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4e2-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb4e2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4e2-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb4e2-142">INPUTS</span></span>

### <span data-ttu-id="fb4e2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fb4e2-143">System.String</span></span>

## <span data-ttu-id="fb4e2-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb4e2-144">OUTPUTS</span></span>

### <span data-ttu-id="fb4e2-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="fb4e2-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="fb4e2-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb4e2-146">NOTES</span></span>

## <span data-ttu-id="fb4e2-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb4e2-147">RELATED LINKS</span></span>
