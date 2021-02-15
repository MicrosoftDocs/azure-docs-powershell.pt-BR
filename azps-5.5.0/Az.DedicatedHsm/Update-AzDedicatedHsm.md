---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116223"
---
# <span data-ttu-id="4ad4f-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="4ad4f-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="4ad4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ad4f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad4f-103">Atualize um HSM dedicado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="4ad4f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ad4f-104">SYNTAX</span></span>

### <span data-ttu-id="4ad4f-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4ad4f-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ad4f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4ad4f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ad4f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4ad4f-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad4f-108">Atualize um HSM dedicado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="4ad4f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4ad4f-109">EXAMPLES</span></span>

### <span data-ttu-id="4ad4f-110">Exemplo 1: Atualizar a marca de parâmetro do HSM Dedicado por nome</span><span class="sxs-lookup"><span data-stu-id="4ad4f-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="4ad4f-111">Este comando atualiza a marca de parâmetro do HSM Dedicado por nome</span><span class="sxs-lookup"><span data-stu-id="4ad4f-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="4ad4f-112">Exemplo 2: Atualizar a marca de parâmetro do HSM Dedicado por objeto</span><span class="sxs-lookup"><span data-stu-id="4ad4f-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="4ad4f-113">Este comando atualiza a marca de parâmetro do HSM Dedicado por objeto</span><span class="sxs-lookup"><span data-stu-id="4ad4f-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="4ad4f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ad4f-114">PARAMETERS</span></span>

### <span data-ttu-id="4ad4f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ad4f-115">-AsJob</span></span>
<span data-ttu-id="4ad4f-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="4ad4f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4ad4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad4f-117">-DefaultProfile</span></span>
<span data-ttu-id="4ad4f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad4f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ad4f-119">-InputObject</span></span>
<span data-ttu-id="4ad4f-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ad4f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ad4f-121">-Name</span></span>
<span data-ttu-id="4ad4f-122">Nome do HSM dedicado</span><span class="sxs-lookup"><span data-stu-id="4ad4f-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="4ad4f-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4ad4f-123">-NoWait</span></span>
<span data-ttu-id="4ad4f-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="4ad4f-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4ad4f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad4f-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ad4f-126">O nome do Grupo de Recursos ao qual o servidor pertence.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="4ad4f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ad4f-127">-SubscriptionId</span></span>
<span data-ttu-id="4ad4f-128">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ad4f-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4ad4f-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4ad4f-130">-Tag</span></span>
<span data-ttu-id="4ad4f-131">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="4ad4f-131">Resource tags</span></span>

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

### <span data-ttu-id="4ad4f-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4ad4f-132">-Confirm</span></span>
<span data-ttu-id="4ad4f-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad4f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad4f-134">-WhatIf</span></span>
<span data-ttu-id="4ad4f-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ad4f-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad4f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad4f-137">CommonParameters</span></span>
<span data-ttu-id="4ad4f-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad4f-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ad4f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad4f-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="4ad4f-140">INPUTS</span></span>

### <span data-ttu-id="4ad4f-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="4ad4f-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="4ad4f-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="4ad4f-142">OUTPUTS</span></span>

### <span data-ttu-id="4ad4f-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="4ad4f-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="4ad4f-144">Notas</span><span class="sxs-lookup"><span data-stu-id="4ad4f-144">NOTES</span></span>

<span data-ttu-id="4ad4f-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="4ad4f-145">ALIASES</span></span>

<span data-ttu-id="4ad4f-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4ad4f-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ad4f-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ad4f-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ad4f-149">INPUTOBJECT: <IDedicatedHsmIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="4ad4f-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ad4f-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4ad4f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ad4f-151">`[Name <String>]`: Nome do Hsm dedicado</span><span class="sxs-lookup"><span data-stu-id="4ad4f-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="4ad4f-152">`[ResourceGroupName <String>]`: o nome do Grupo de Recursos ao qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="4ad4f-153">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4ad4f-154">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4ad4f-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4ad4f-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ad4f-155">RELATED LINKS</span></span>

