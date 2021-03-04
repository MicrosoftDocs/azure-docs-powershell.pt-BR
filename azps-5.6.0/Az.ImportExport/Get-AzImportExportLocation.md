---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: 928ac0254619a2924421a0b52bf20212b8ba19a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886759"
---
# <span data-ttu-id="e3afe-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="e3afe-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="e3afe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3afe-102">SYNOPSIS</span></span>
<span data-ttu-id="e3afe-103">Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="e3afe-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="e3afe-104">Um local é uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3afe-104">A location is an Azure region.</span></span>

## <span data-ttu-id="e3afe-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3afe-105">SYNTAX</span></span>

### <span data-ttu-id="e3afe-106">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e3afe-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e3afe-107">Obter</span><span class="sxs-lookup"><span data-stu-id="e3afe-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3afe-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3afe-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e3afe-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3afe-109">DESCRIPTION</span></span>
<span data-ttu-id="e3afe-110">Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="e3afe-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="e3afe-111">Um local é uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3afe-111">A location is an Azure region.</span></span>

## <span data-ttu-id="e3afe-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3afe-112">EXAMPLES</span></span>

### <span data-ttu-id="e3afe-113">Exemplo 1: Obter todos os detalhes de local da região do Azure com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="e3afe-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="e3afe-114">Este cmdlet obtém todos os detalhes de local da região do Azure com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="e3afe-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="e3afe-115">Exemplo 2: Obter detalhes de local da região do Azure pelo nome do local</span><span class="sxs-lookup"><span data-stu-id="e3afe-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="e3afe-116">Este cmdlet obtém os detalhes do local da região do Azure pelo nome do local.</span><span class="sxs-lookup"><span data-stu-id="e3afe-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="e3afe-117">Exemplo 3: Obter detalhes de local da região do Azure por identidade</span><span class="sxs-lookup"><span data-stu-id="e3afe-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="e3afe-118">Este cmdlet lista os detalhes de local da região do Azure por identidade.</span><span class="sxs-lookup"><span data-stu-id="e3afe-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="e3afe-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3afe-119">PARAMETERS</span></span>

### <span data-ttu-id="e3afe-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e3afe-120">-AcceptLanguage</span></span>
<span data-ttu-id="e3afe-121">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="e3afe-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="e3afe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3afe-122">-DefaultProfile</span></span>
<span data-ttu-id="e3afe-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3afe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3afe-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3afe-124">-InputObject</span></span>
<span data-ttu-id="e3afe-125">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e3afe-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3afe-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e3afe-126">-Name</span></span>
<span data-ttu-id="e3afe-127">O nome do local.</span><span class="sxs-lookup"><span data-stu-id="e3afe-127">The name of the location.</span></span>
<span data-ttu-id="e3afe-128">Por exemplo, West US ou westus.</span><span class="sxs-lookup"><span data-stu-id="e3afe-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3afe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3afe-129">CommonParameters</span></span>
<span data-ttu-id="e3afe-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3afe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3afe-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3afe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3afe-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3afe-132">INPUTS</span></span>

### <span data-ttu-id="e3afe-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="e3afe-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="e3afe-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3afe-134">OUTPUTS</span></span>

### <span data-ttu-id="e3afe-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span><span class="sxs-lookup"><span data-stu-id="e3afe-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="e3afe-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3afe-136">NOTES</span></span>

<span data-ttu-id="e3afe-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e3afe-137">ALIASES</span></span>

<span data-ttu-id="e3afe-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="e3afe-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3afe-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="e3afe-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3afe-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3afe-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3afe-141">INPUTOBJECT <IImportExportIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="e3afe-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3afe-142">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="e3afe-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3afe-143">`[JobName <String>]`: O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="e3afe-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="e3afe-144">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="e3afe-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="e3afe-145">Por exemplo, West US ou westus.</span><span class="sxs-lookup"><span data-stu-id="e3afe-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="e3afe-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3afe-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="e3afe-147">`[SubscriptionId <String>]`: A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3afe-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="e3afe-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3afe-148">RELATED LINKS</span></span>

