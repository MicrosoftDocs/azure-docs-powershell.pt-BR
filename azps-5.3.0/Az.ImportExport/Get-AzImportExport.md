---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433766"
---
# <span data-ttu-id="2f7b5-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="2f7b5-101">Get-AzImportExport</span></span>

## <span data-ttu-id="2f7b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2f7b5-103">Obtém informações sobre um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="2f7b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f7b5-104">SYNTAX</span></span>

### <span data-ttu-id="2f7b5-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="2f7b5-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2f7b5-106">Obter</span><span class="sxs-lookup"><span data-stu-id="2f7b5-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2f7b5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2f7b5-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2f7b5-108">List1</span><span class="sxs-lookup"><span data-stu-id="2f7b5-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2f7b5-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f7b5-109">DESCRIPTION</span></span>
<span data-ttu-id="2f7b5-110">Obtém informações sobre um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="2f7b5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f7b5-111">EXAMPLES</span></span>

### <span data-ttu-id="2f7b5-112">Exemplo 1: obter o trabalho do ImportExport com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="2f7b5-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2f7b5-113">Esse cmdlet obtém um trabalho ImportExport com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="2f7b5-114">Exemplo 2: obter ImportExport trabalho por grupo de recursos e nome do trabalho</span><span class="sxs-lookup"><span data-stu-id="2f7b5-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2f7b5-115">Esse cmdlet obtém um trabalho do ImportExport por grupo de recursos e nome do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="2f7b5-116">Exemplo 3: lista todos os trabalhos do ImportExport no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="2f7b5-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2f7b5-117">Esse cmdlet lista todos os trabalhos do ImportExport no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="2f7b5-118">Exemplo 4: obter ImportExport de trabalho por identidade</span><span class="sxs-lookup"><span data-stu-id="2f7b5-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="2f7b5-119">Esta lista de cmdlets Obtém o trabalho do ImportExport por identidade.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="2f7b5-120">OS</span><span class="sxs-lookup"><span data-stu-id="2f7b5-120">PARAMETERS</span></span>

### <span data-ttu-id="2f7b5-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="2f7b5-121">-AcceptLanguage</span></span>
<span data-ttu-id="2f7b5-122">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="2f7b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f7b5-123">-DefaultProfile</span></span>
<span data-ttu-id="2f7b5-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f7b5-125">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2f7b5-125">-Filter</span></span>
<span data-ttu-id="2f7b5-126">Pode ser usado para restringir os resultados a determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f7b5-127">-InputObject</span></span>
<span data-ttu-id="2f7b5-128">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f7b5-129">-Name</span></span>
<span data-ttu-id="2f7b5-130">O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f7b5-131">-ResourceGroupName</span></span>
<span data-ttu-id="2f7b5-132">O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f7b5-133">-SubscriptionId</span></span>
<span data-ttu-id="2f7b5-134">A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-135">-Início</span><span class="sxs-lookup"><span data-stu-id="2f7b5-135">-Top</span></span>
<span data-ttu-id="2f7b5-136">Um valor inteiro que especifica o número de trabalhos no máximo deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="2f7b5-137">O valor não pode exceder 100.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f7b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f7b5-138">CommonParameters</span></span>
<span data-ttu-id="2f7b5-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f7b5-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f7b5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f7b5-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f7b5-141">INPUTS</span></span>

### <span data-ttu-id="2f7b5-142">Microsoft. Azure. PowerShell. cmdlets. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="2f7b5-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="2f7b5-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f7b5-143">OUTPUTS</span></span>

### <span data-ttu-id="2f7b5-144">Microsoft. Azure. PowerShell. cmdlets. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="2f7b5-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="2f7b5-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f7b5-145">NOTES</span></span>

<span data-ttu-id="2f7b5-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2f7b5-146">ALIASES</span></span>

<span data-ttu-id="2f7b5-147">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="2f7b5-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2f7b5-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f7b5-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2f7b5-150">INPUTobject <IImportExportIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="2f7b5-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2f7b5-151">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="2f7b5-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f7b5-152">`[JobName <String>]`: O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="2f7b5-153">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="2f7b5-154">Por exemplo, Oeste EUA ou oesteus.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="2f7b5-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="2f7b5-156">`[SubscriptionId <String>]`: A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f7b5-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="2f7b5-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f7b5-157">RELATED LINKS</span></span>

