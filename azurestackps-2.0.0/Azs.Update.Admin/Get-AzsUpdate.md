---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775202"
---
# <span data-ttu-id="49236-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="49236-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="49236-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49236-102">SYNOPSIS</span></span>
<span data-ttu-id="49236-103">Obtenha uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="49236-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="49236-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49236-104">SYNTAX</span></span>

### <span data-ttu-id="49236-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="49236-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49236-106">Obter</span><span class="sxs-lookup"><span data-stu-id="49236-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49236-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49236-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="49236-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="49236-108">DESCRIPTION</span></span>
<span data-ttu-id="49236-109">Obtenha uma atualização específica em um local de atualização.</span><span class="sxs-lookup"><span data-stu-id="49236-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="49236-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="49236-110">EXAMPLES</span></span>

### <span data-ttu-id="49236-111">Exemplo 1: obter todas as atualizações</span><span class="sxs-lookup"><span data-stu-id="49236-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="49236-112">Sem parâmetros, Get-AzsUpdate listará todas as atualizações que o carimbo pode descobrir</span><span class="sxs-lookup"><span data-stu-id="49236-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="49236-113">Exemplo 2: obter atualização por nome</span><span class="sxs-lookup"><span data-stu-id="49236-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="49236-114">Recuperará todas as atualizações correspondentes ao nome especificado</span><span class="sxs-lookup"><span data-stu-id="49236-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="49236-115">Exemplo 3: obter todas as atualizações por local</span><span class="sxs-lookup"><span data-stu-id="49236-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="49236-116">Recuperará todas as atualizações em um local especificado.</span><span class="sxs-lookup"><span data-stu-id="49236-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="49236-117">No momento, só há suporte para um local, portanto, esse é o equivalente a apenas Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="49236-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="49236-118">OS</span><span class="sxs-lookup"><span data-stu-id="49236-118">PARAMETERS</span></span>

### <span data-ttu-id="49236-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49236-119">-DefaultProfile</span></span>
<span data-ttu-id="49236-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49236-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49236-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49236-121">-InputObject</span></span>
<span data-ttu-id="49236-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="49236-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="49236-123">-Local</span><span class="sxs-lookup"><span data-stu-id="49236-123">-Location</span></span>
<span data-ttu-id="49236-124">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="49236-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="49236-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="49236-125">-Name</span></span>
<span data-ttu-id="49236-126">Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="49236-126">Name of the update.</span></span>

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

### <span data-ttu-id="49236-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49236-127">-ResourceGroupName</span></span>
<span data-ttu-id="49236-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49236-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="49236-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49236-129">-SubscriptionId</span></span>
<span data-ttu-id="49236-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49236-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="49236-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="49236-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="49236-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49236-132">CommonParameters</span></span>
<span data-ttu-id="49236-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49236-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49236-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49236-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49236-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="49236-135">INPUTS</span></span>

### <span data-ttu-id="49236-136">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="49236-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="49236-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="49236-137">OUTPUTS</span></span>

### <span data-ttu-id="49236-138">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. Api20160501. IUpdate</span><span class="sxs-lookup"><span data-stu-id="49236-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="49236-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="49236-139">NOTES</span></span>

<span data-ttu-id="49236-140">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="49236-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49236-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49236-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="49236-142">INPUTobject <IUpdateAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="49236-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49236-143">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="49236-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49236-144">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="49236-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="49236-145">`[RunName <String>]`: Atualizar identificador de execução.</span><span class="sxs-lookup"><span data-stu-id="49236-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="49236-146">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49236-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="49236-147">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="49236-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="49236-148">`[UpdateLocation <String>]`: O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="49236-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="49236-149">`[UpdateName <String>]`: Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="49236-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="49236-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49236-150">RELATED LINKS</span></span>

