---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112749"
---
# <span data-ttu-id="8dbc6-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="8dbc6-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="8dbc6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8dbc6-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbc6-103">Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="8dbc6-104">Um local é uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-104">A location is an Azure region.</span></span>

## <span data-ttu-id="8dbc6-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dbc6-105">SYNTAX</span></span>

### <span data-ttu-id="8dbc6-106">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="8dbc6-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8dbc6-107">Obter</span><span class="sxs-lookup"><span data-stu-id="8dbc6-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8dbc6-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8dbc6-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8dbc6-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8dbc6-109">DESCRIPTION</span></span>
<span data-ttu-id="8dbc6-110">Retorna os detalhes sobre um local para o qual você pode enviar os discos associados a um trabalho de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="8dbc6-111">Um local é uma região do Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-111">A location is an Azure region.</span></span>

## <span data-ttu-id="8dbc6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8dbc6-112">EXAMPLES</span></span>

### <span data-ttu-id="8dbc6-113">Exemplo 1: obter todos os detalhes de localização da região do Azure com contexto padrão</span><span class="sxs-lookup"><span data-stu-id="8dbc6-113">Example 1: Get all Azure region location details with default context</span></span>
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

<span data-ttu-id="8dbc6-114">Este cmdlet obtém todos os detalhes de localização da região do Azure com contexto padrão.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="8dbc6-115">Exemplo 2: obter detalhes de localização da região do Azure por nome do local</span><span class="sxs-lookup"><span data-stu-id="8dbc6-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="8dbc6-116">Esse cmdlet obtém detalhes de localização da região do Azure por nome de localização.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="8dbc6-117">Exemplo 3: obter detalhes de localização da região do Azure por identidade</span><span class="sxs-lookup"><span data-stu-id="8dbc6-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="8dbc6-118">Esta lista de cmdlets Obtém detalhes de localização da região do Azure por identidade.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="8dbc6-119">OS</span><span class="sxs-lookup"><span data-stu-id="8dbc6-119">PARAMETERS</span></span>

### <span data-ttu-id="8dbc6-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="8dbc6-120">-AcceptLanguage</span></span>
<span data-ttu-id="8dbc6-121">Especifica o idioma preferencial para a resposta.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-121">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="8dbc6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbc6-122">-DefaultProfile</span></span>
<span data-ttu-id="8dbc6-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dbc6-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dbc6-124">-InputObject</span></span>
<span data-ttu-id="8dbc6-125">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8dbc6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8dbc6-126">-Name</span></span>
<span data-ttu-id="8dbc6-127">O nome do local.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-127">The name of the location.</span></span>
<span data-ttu-id="8dbc6-128">Por exemplo, Oeste EUA ou oesteus.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-128">For example, West US or westus.</span></span>

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

### <span data-ttu-id="8dbc6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbc6-129">CommonParameters</span></span>
<span data-ttu-id="8dbc6-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbc6-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dbc6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbc6-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8dbc6-132">INPUTS</span></span>

### <span data-ttu-id="8dbc6-133">Microsoft. Azure. PowerShell. cmdlets. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="8dbc6-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="8dbc6-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8dbc6-134">OUTPUTS</span></span>

### <span data-ttu-id="8dbc6-135">Microsoft. Azure. PowerShell. cmdlets. ImportExport. Models. Api20161101. ILocation</span><span class="sxs-lookup"><span data-stu-id="8dbc6-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="8dbc6-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8dbc6-136">NOTES</span></span>

<span data-ttu-id="8dbc6-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8dbc6-137">ALIASES</span></span>

<span data-ttu-id="8dbc6-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="8dbc6-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8dbc6-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8dbc6-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8dbc6-141">INPUTobject <IImportExportIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="8dbc6-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8dbc6-142">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="8dbc6-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8dbc6-143">`[JobName <String>]`: O nome do trabalho de importação/exportação.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="8dbc6-144">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="8dbc6-145">Por exemplo, Oeste EUA ou oesteus.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="8dbc6-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="8dbc6-147">`[SubscriptionId <String>]`: A ID da assinatura do usuário do Azure.</span><span class="sxs-lookup"><span data-stu-id="8dbc6-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="8dbc6-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8dbc6-148">RELATED LINKS</span></span>

