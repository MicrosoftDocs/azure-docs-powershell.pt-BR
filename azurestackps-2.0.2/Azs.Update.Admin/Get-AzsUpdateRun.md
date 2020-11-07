---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdaterun
schema: 2.0.0
ms.openlocfilehash: fb36cb0d1be46abb66a1c0cc97165f8eb9cc3913
ms.sourcegitcommit: f7edd4f5c4bebedc139cb01438081edc6ed560bd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/29/2020
ms.locfileid: "93947349"
---
# <span data-ttu-id="ee297-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="ee297-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="ee297-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee297-102">SYNOPSIS</span></span>
<span data-ttu-id="ee297-103">Obtenha uma instância de Update Run usando a ID.</span><span class="sxs-lookup"><span data-stu-id="ee297-103">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="ee297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee297-104">SYNTAX</span></span>

### <span data-ttu-id="ee297-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="ee297-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee297-106">Obter</span><span class="sxs-lookup"><span data-stu-id="ee297-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ee297-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ee297-107">GetViaIdentity</span></span>
```
Get-AzsUpdateRun -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ee297-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee297-108">DESCRIPTION</span></span>
<span data-ttu-id="ee297-109">Obtenha uma instância de Update Run usando a ID.</span><span class="sxs-lookup"><span data-stu-id="ee297-109">Get an instance of update run using the ID.</span></span>

## <span data-ttu-id="ee297-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee297-110">EXAMPLES</span></span>

### <span data-ttu-id="ee297-111">Exemplo 1: Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="ee297-111">Example 1: Get-AzsUpdateRun</span></span>
```powershell
PS C:\> Get-AzsUpdateRun

cmdlet Get-AzsUpdateRun at command pipeline position 1
Supply values for the following parameters:
UpdateName: Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="ee297-112">Se um valor updatename não for especificado, Get-UpdateRun sempre pedirá entrada.</span><span class="sxs-lookup"><span data-stu-id="ee297-112">If a UpdateName value is not specified, Get-UpdateRun will always ask for input.</span></span>
<span data-ttu-id="ee297-113">Uma vez fornecido, ele produzirá todas as instâncias de UpdateRun com falha ou bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="ee297-113">Once provided, it will output all instances of UpdateRun that were Failed or Successful</span></span>

### <span data-ttu-id="ee297-114">Exemplo 2: Get-AzsUpdateRun por updatename</span><span class="sxs-lookup"><span data-stu-id="ee297-114">Example 2: Get-AzsUpdateRun By UpdateName</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
northwest/Microsoft1.1907.0.10/51e878... Succeeded       7/11/2019 3:07:10 PM      7/12/2019 6:47:37 AM
```

<span data-ttu-id="ee297-115">Vai recuperar todos os UpdateRuns associados a uma atualização específica</span><span class="sxs-lookup"><span data-stu-id="ee297-115">Will retrieve all UpdateRuns associated with a specific Update</span></span>

### <span data-ttu-id="ee297-116">Exemplo 2: Get-AzsUpdateRun por nome</span><span class="sxs-lookup"><span data-stu-id="ee297-116">Example 2: Get-AzsUpdateRun By Name</span></span>
```powershell
PS C:\> Get-AzsUpdateRun -UpdateName Microsoft1.1907.0.10 -Name 45aaeb26-805b-495b-9c8c-d5da5542dbf4
or 
PS C:\> Get-AzsUpdateRun -UpdateName northwest/Microsoft1.1907.0.10 -Name northwest/Microsoft1.1907.0.10/45aaeb26-805b-495b-9c8c-d5da5542dbf4

Name                                     State           ProgressStartTimeUtc      ProgressEndTimeUtc
----                                     -----           --------------------      ------------------
northwest/Microsoft1.1907.0.10/45aaeb... Failed          7/11/2019 3:07:10 PM      7/11/2019 7:38:05 PM
```

<span data-ttu-id="ee297-117">Recuperará todos os UpdateRuns associados a uma atualização específica e um nome específico</span><span class="sxs-lookup"><span data-stu-id="ee297-117">Will retrieve all UpdateRuns associated with a specific Update and a specific Name</span></span>

## <span data-ttu-id="ee297-118">OS</span><span class="sxs-lookup"><span data-stu-id="ee297-118">PARAMETERS</span></span>

### <span data-ttu-id="ee297-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee297-119">-DefaultProfile</span></span>
<span data-ttu-id="ee297-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ee297-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee297-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee297-121">-InputObject</span></span>
<span data-ttu-id="ee297-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="ee297-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee297-123">-Local</span><span class="sxs-lookup"><span data-stu-id="ee297-123">-Location</span></span>
<span data-ttu-id="ee297-124">O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="ee297-124">The name of the update location.</span></span>

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

### <span data-ttu-id="ee297-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee297-125">-Name</span></span>
<span data-ttu-id="ee297-126">Identificador de execução de atualização.</span><span class="sxs-lookup"><span data-stu-id="ee297-126">Update run identifier.</span></span>

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

### <span data-ttu-id="ee297-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee297-127">-ResourceGroupName</span></span>
<span data-ttu-id="ee297-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee297-128">Resource group name.</span></span>

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

### <span data-ttu-id="ee297-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee297-129">-SubscriptionId</span></span>
<span data-ttu-id="ee297-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee297-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ee297-131">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ee297-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ee297-132">-Updatename</span><span class="sxs-lookup"><span data-stu-id="ee297-132">-UpdateName</span></span>
<span data-ttu-id="ee297-133">Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="ee297-133">Name of the update.</span></span>

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

### <span data-ttu-id="ee297-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee297-134">CommonParameters</span></span>
<span data-ttu-id="ee297-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee297-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee297-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee297-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee297-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee297-137">INPUTS</span></span>

### <span data-ttu-id="ee297-138">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ee297-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="ee297-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee297-139">OUTPUTS</span></span>

### <span data-ttu-id="ee297-140">Microsoft. Azure. PowerShell. cmdlets. UpdateAdmin. Models. Api20160501. IUpdateRun</span><span class="sxs-lookup"><span data-stu-id="ee297-140">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateRun</span></span>



## <span data-ttu-id="ee297-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee297-141">NOTES</span></span>

<span data-ttu-id="ee297-142">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="ee297-142">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee297-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee297-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ee297-144">INPUTobject <IUpdateAdminIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="ee297-144">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ee297-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="ee297-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ee297-146">`[ResourceGroupName <String>]`: Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ee297-146">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="ee297-147">`[RunName <String>]`: Atualizar identificador de execução.</span><span class="sxs-lookup"><span data-stu-id="ee297-147">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="ee297-148">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ee297-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="ee297-149">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="ee297-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ee297-150">`[UpdateLocation <String>]`: O nome do local de atualização.</span><span class="sxs-lookup"><span data-stu-id="ee297-150">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="ee297-151">`[UpdateName <String>]`: Nome da atualização.</span><span class="sxs-lookup"><span data-stu-id="ee297-151">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="ee297-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee297-152">RELATED LINKS</span></span>

