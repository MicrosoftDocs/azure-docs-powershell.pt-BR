---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775199"
---
# <span data-ttu-id="f7361-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="f7361-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="f7361-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7361-102">SYNOPSIS</span></span>
<span data-ttu-id="f7361-103">Obtenha um local de atualização com base no nome.</span><span class="sxs-lookup"><span data-stu-id="f7361-103">Get an update location based on name.</span></span>

## <span data-ttu-id="f7361-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7361-104">SYNTAX</span></span>

### <span data-ttu-id="f7361-105">Get (padrão)</span><span class="sxs-lookup"><span data-stu-id="f7361-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f7361-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f7361-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f7361-107">Programação</span><span class="sxs-lookup"><span data-stu-id="f7361-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7361-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7361-108">DESCRIPTION</span></span>
<span data-ttu-id="f7361-109">Obtenha um local de atualização com base no nome.</span><span class="sxs-lookup"><span data-stu-id="f7361-109">Get an update location based on name.</span></span>

## <span data-ttu-id="f7361-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7361-110">EXAMPLES</span></span>

### <span data-ttu-id="f7361-111">Exemplo 1: obter todos os locais de atualizações</span><span class="sxs-lookup"><span data-stu-id="f7361-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="f7361-112">Sem parâmetros, esse commandlet irá recuperar todos os locais de atualização</span><span class="sxs-lookup"><span data-stu-id="f7361-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="f7361-113">Exemplo 2: obter todos os locais de atualizações por nome</span><span class="sxs-lookup"><span data-stu-id="f7361-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="f7361-114">Recuperará todos os locais de atualização que correspondam ao parâmetro de nome especificado</span><span class="sxs-lookup"><span data-stu-id="f7361-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="f7361-115">OS</span><span class="sxs-lookup"><span data-stu-id="f7361-115">PARAMETERS</span></span>

### <span data-ttu-id="f7361-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7361-116">-DefaultProfile</span></span>
<span data-ttu-id="f7361-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7361-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7361-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7361-118">-InputObject</span></span>
<span data-ttu-id="f7361-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f7361-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f7361-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7361-120">-Name</span></span>
<span data-ttu-id="f7361-121">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="f7361-121">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f7361-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7361-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7361-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7361-123">Resource group name.</span></span>

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

### <span data-ttu-id="f7361-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7361-124">-SubscriptionId</span></span>
<span data-ttu-id="f7361-125">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f7361-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f7361-126">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f7361-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f7361-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7361-127">CommonParameters</span></span>
<span data-ttu-id="f7361-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7361-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7361-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7361-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7361-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7361-130">INPUTS</span></span>

### <span data-ttu-id="f7361-131">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f7361-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="f7361-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7361-132">OUTPUTS</span></span>

### <span data-ttu-id="f7361-133">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="f7361-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="f7361-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7361-134">NOTES</span></span>

<span data-ttu-id="f7361-135">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f7361-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7361-136">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7361-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f7361-137">INPUTobject <IUpdateAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f7361-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7361-138">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f7361-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7361-139">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f7361-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="f7361-140">`[RunName <String>]`: Atualizar identificador de execução.</span><span class="sxs-lookup"><span data-stu-id="f7361-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="f7361-141">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f7361-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="f7361-142">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f7361-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f7361-143">`[UpdateLocation <String>]`: O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="f7361-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="f7361-144">`[UpdateName <String>]`: Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="f7361-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="f7361-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7361-145">RELATED LINKS</span></span>

