---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 8825cb9b3d4a2efcd6a326244139950e431d71f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886965"
---
# <span data-ttu-id="7351e-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="7351e-101">Get-AzImportExport</span></span>

## <span data-ttu-id="7351e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7351e-102">SYNOPSIS</span></span>
<span data-ttu-id="7351e-103">Obtém informações sobre um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="7351e-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="7351e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7351e-104">SYNTAX</span></span>

### <span data-ttu-id="7351e-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7351e-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7351e-106">Obter</span><span class="sxs-lookup"><span data-stu-id="7351e-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7351e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7351e-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7351e-108">List1</span><span class="sxs-lookup"><span data-stu-id="7351e-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7351e-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7351e-109">DESCRIPTION</span></span>
<span data-ttu-id="7351e-110">Obtém informações sobre um trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="7351e-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="7351e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7351e-111">EXAMPLES</span></span>

### <span data-ttu-id="7351e-112">Exemplo 1: Obter trabalho ImportExport com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="7351e-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="7351e-113">Este cmdlet obtém trabalho ImportExport com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="7351e-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="7351e-114">Exemplo 2: Obter trabalho ImportExport por grupo de recursos e nome de trabalho</span><span class="sxs-lookup"><span data-stu-id="7351e-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="7351e-115">Este cmdlet obtém o trabalho ImportExport por grupo de recursos e nome de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7351e-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="7351e-116">Exemplo 3: lista todos os trabalhos ImportExport no grupo de recursos especificado</span><span class="sxs-lookup"><span data-stu-id="7351e-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="7351e-117">Este cmdlet lista todos os trabalhos ImportExport no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="7351e-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="7351e-118">Exemplo 4: Obter trabalho ImportExport por identidade</span><span class="sxs-lookup"><span data-stu-id="7351e-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="7351e-119">Este cmdlet lists obtém o trabalho ImportExport por identidade.</span><span class="sxs-lookup"><span data-stu-id="7351e-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="7351e-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7351e-120">PARAMETERS</span></span>

### <span data-ttu-id="7351e-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="7351e-121">-AcceptLanguage</span></span>
<span data-ttu-id="7351e-122">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="7351e-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="7351e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7351e-123">-DefaultProfile</span></span>
<span data-ttu-id="7351e-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7351e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7351e-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="7351e-125">-Filter</span></span>
<span data-ttu-id="7351e-126">Pode ser usado para restringir os resultados a determinadas condições.</span><span class="sxs-lookup"><span data-stu-id="7351e-126">Can be used to restrict the results to certain conditions.</span></span>

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

### <span data-ttu-id="7351e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7351e-127">-InputObject</span></span>
<span data-ttu-id="7351e-128">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="7351e-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7351e-129">-Name</span><span class="sxs-lookup"><span data-stu-id="7351e-129">-Name</span></span>
<span data-ttu-id="7351e-130">O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="7351e-130">The name of the import/export job.</span></span>

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

### <span data-ttu-id="7351e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7351e-131">-ResourceGroupName</span></span>
<span data-ttu-id="7351e-132">O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="7351e-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="7351e-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7351e-133">-SubscriptionId</span></span>
<span data-ttu-id="7351e-134">A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="7351e-134">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="7351e-135">-Top</span><span class="sxs-lookup"><span data-stu-id="7351e-135">-Top</span></span>
<span data-ttu-id="7351e-136">Um valor inteiro que especifica quantos trabalhos, no máximo, devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="7351e-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="7351e-137">O valor não pode exceder 100.</span><span class="sxs-lookup"><span data-stu-id="7351e-137">The value cannot exceed 100.</span></span>

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

### <span data-ttu-id="7351e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7351e-138">CommonParameters</span></span>
<span data-ttu-id="7351e-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7351e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7351e-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7351e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7351e-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7351e-141">INPUTS</span></span>

### <span data-ttu-id="7351e-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="7351e-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="7351e-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7351e-143">OUTPUTS</span></span>

### <span data-ttu-id="7351e-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="7351e-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="7351e-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="7351e-145">NOTES</span></span>

<span data-ttu-id="7351e-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7351e-146">ALIASES</span></span>

<span data-ttu-id="7351e-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="7351e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7351e-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="7351e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7351e-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7351e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7351e-150">INPUTOBJECT <IImportExportIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="7351e-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7351e-151">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="7351e-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7351e-152">`[JobName <String>]`: O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="7351e-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="7351e-153">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="7351e-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="7351e-154">Por exemplo, West US ou westus.</span><span class="sxs-lookup"><span data-stu-id="7351e-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="7351e-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="7351e-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="7351e-156">`[SubscriptionId <String>]`: A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="7351e-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="7351e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7351e-157">RELATED LINKS</span></span>

