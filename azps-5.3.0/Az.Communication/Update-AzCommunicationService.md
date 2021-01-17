---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434395"
---
# <span data-ttu-id="762bc-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="762bc-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="762bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="762bc-102">SYNOPSIS</span></span>
<span data-ttu-id="762bc-103">Operação para atualizar um CommunicationService existente.</span><span class="sxs-lookup"><span data-stu-id="762bc-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="762bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="762bc-104">SYNTAX</span></span>

### <span data-ttu-id="762bc-105">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="762bc-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="762bc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="762bc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="762bc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="762bc-107">DESCRIPTION</span></span>
<span data-ttu-id="762bc-108">Operação para atualizar um CommunicationService existente.</span><span class="sxs-lookup"><span data-stu-id="762bc-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="762bc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="762bc-109">EXAMPLES</span></span>

### <span data-ttu-id="762bc-110">Exemplo 1: atualizar um recurso existente do ACS para ter marcas</span><span class="sxs-lookup"><span data-stu-id="762bc-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="762bc-111">Anexa as marcas fornecidas ao recurso ACS especificado.</span><span class="sxs-lookup"><span data-stu-id="762bc-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="762bc-112">OS</span><span class="sxs-lookup"><span data-stu-id="762bc-112">PARAMETERS</span></span>

### <span data-ttu-id="762bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762bc-113">-DefaultProfile</span></span>
<span data-ttu-id="762bc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="762bc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="762bc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="762bc-115">-InputObject</span></span>
<span data-ttu-id="762bc-116">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="762bc-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="762bc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="762bc-117">-Name</span></span>
<span data-ttu-id="762bc-118">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="762bc-118">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="762bc-120">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="762bc-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="762bc-121">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="762bc-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="762bc-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="762bc-122">-SubscriptionId</span></span>
<span data-ttu-id="762bc-123">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="762bc-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="762bc-124">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="762bc-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="762bc-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="762bc-125">-Tag</span></span>
<span data-ttu-id="762bc-126">Marcas do serviço que é uma lista de pares de valores chave que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="762bc-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="762bc-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="762bc-127">-Confirm</span></span>
<span data-ttu-id="762bc-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="762bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="762bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762bc-129">-WhatIf</span></span>
<span data-ttu-id="762bc-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="762bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="762bc-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="762bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="762bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762bc-132">CommonParameters</span></span>
<span data-ttu-id="762bc-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762bc-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="762bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762bc-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="762bc-135">INPUTS</span></span>

### <span data-ttu-id="762bc-136">Microsoft. Azure. PowerShell. cmdlets. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="762bc-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="762bc-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="762bc-137">OUTPUTS</span></span>

### <span data-ttu-id="762bc-138">Microsoft. Azure. PowerShell. cmdlets. Communication. Models. Api20200820Preview. ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="762bc-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="762bc-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="762bc-139">NOTES</span></span>

<span data-ttu-id="762bc-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="762bc-140">ALIASES</span></span>

<span data-ttu-id="762bc-141">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="762bc-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="762bc-142">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="762bc-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="762bc-143">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="762bc-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="762bc-144">INPUTobject <ICommunicationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="762bc-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="762bc-145">`[CommunicationServiceName <String>]`: O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="762bc-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="762bc-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="762bc-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="762bc-147">`[Location <String>]`: A região do Azure</span><span class="sxs-lookup"><span data-stu-id="762bc-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="762bc-148">`[OperationId <String>]`: A ID de uma operação assíncrona em andamento</span><span class="sxs-lookup"><span data-stu-id="762bc-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="762bc-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="762bc-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="762bc-150">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="762bc-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="762bc-151">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="762bc-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="762bc-152">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="762bc-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="762bc-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="762bc-153">RELATED LINKS</span></span>

