---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256886"
---
# <span data-ttu-id="b6ba4-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b6ba4-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="b6ba4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ba4-103">Atualize um HSM exclusivo na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="b6ba4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6ba4-104">SYNTAX</span></span>

### <span data-ttu-id="b6ba4-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6ba4-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6ba4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b6ba4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6ba4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6ba4-107">DESCRIPTION</span></span>
<span data-ttu-id="b6ba4-108">Atualize um HSM exclusivo na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="b6ba4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6ba4-109">EXAMPLES</span></span>

### <span data-ttu-id="b6ba4-110">Exemplo 1: atualizar a marca de parâmetro do HSM dedicado por nome</span><span class="sxs-lookup"><span data-stu-id="b6ba4-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b6ba4-111">Esse comando atualiza a marca de parâmetro do HSM dedicado por nome</span><span class="sxs-lookup"><span data-stu-id="b6ba4-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="b6ba4-112">Exemplo 2: atualizar a marca de parâmetro do HSM dedicado por objeto</span><span class="sxs-lookup"><span data-stu-id="b6ba4-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b6ba4-113">Esse comando atualiza a marca de parâmetro do HSM dedicado por objeto</span><span class="sxs-lookup"><span data-stu-id="b6ba4-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="b6ba4-114">OS</span><span class="sxs-lookup"><span data-stu-id="b6ba4-114">PARAMETERS</span></span>

### <span data-ttu-id="b6ba4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6ba4-115">-AsJob</span></span>
<span data-ttu-id="b6ba4-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b6ba4-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ba4-117">-DefaultProfile</span></span>
<span data-ttu-id="b6ba4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6ba4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6ba4-119">-InputObject</span></span>
<span data-ttu-id="b6ba4-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6ba4-121">-Name</span></span>
<span data-ttu-id="b6ba4-122">Nome do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="b6ba4-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b6ba4-123">-NoWait</span></span>
<span data-ttu-id="b6ba4-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="b6ba4-124">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ba4-125">-ResourceGroupName</span></span>
<span data-ttu-id="b6ba4-126">O nome do grupo de recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6ba4-127">-SubscriptionId</span></span>
<span data-ttu-id="b6ba4-128">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b6ba4-129">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="b6ba4-130">-Tag</span></span>
<span data-ttu-id="b6ba4-131">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="b6ba4-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6ba4-132">-Confirm</span></span>
<span data-ttu-id="b6ba4-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ba4-134">-WhatIf</span></span>
<span data-ttu-id="b6ba4-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6ba4-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6ba4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ba4-137">CommonParameters</span></span>
<span data-ttu-id="b6ba4-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ba4-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6ba4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ba4-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6ba4-140">INPUTS</span></span>

### <span data-ttu-id="b6ba4-141">Microsoft. Azure. PowerShell. cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="b6ba4-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="b6ba4-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6ba4-142">OUTPUTS</span></span>

### <span data-ttu-id="b6ba4-143">Microsoft. Azure. PowerShell. cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b6ba4-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="b6ba4-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6ba4-144">NOTES</span></span>

<span data-ttu-id="b6ba4-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b6ba4-145">ALIASES</span></span>

<span data-ttu-id="b6ba4-146">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="b6ba4-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6ba4-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6ba4-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6ba4-149">INPUTobject <IDedicatedHsmIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="b6ba4-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6ba4-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="b6ba4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6ba4-151">`[Name <String>]`: Nome do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="b6ba4-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="b6ba4-152">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="b6ba4-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b6ba4-154">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b6ba4-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b6ba4-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6ba4-155">RELATED LINKS</span></span>

