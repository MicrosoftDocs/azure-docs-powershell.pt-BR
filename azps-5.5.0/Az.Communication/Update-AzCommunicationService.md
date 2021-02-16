---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/update-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Update-AzCommunicationService.md
ms.openlocfilehash: 717c0981397ecbf419edbaa9f62bcc66443946fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117885"
---
# <span data-ttu-id="3ca66-101">Update-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="3ca66-101">Update-AzCommunicationService</span></span>

## <span data-ttu-id="3ca66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ca66-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca66-103">Operação para atualizar um CommunicationService existente.</span><span class="sxs-lookup"><span data-stu-id="3ca66-103">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="3ca66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ca66-104">SYNTAX</span></span>

### <span data-ttu-id="3ca66-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ca66-105">UpdateExpanded (Default)</span></span>
```
Update-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ca66-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3ca66-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzCommunicationService -InputObject <ICommunicationIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ca66-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ca66-107">DESCRIPTION</span></span>
<span data-ttu-id="3ca66-108">Operação para atualizar um CommunicationService existente.</span><span class="sxs-lookup"><span data-stu-id="3ca66-108">Operation to update an existing CommunicationService.</span></span>

## <span data-ttu-id="3ca66-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3ca66-109">EXAMPLES</span></span>

### <span data-ttu-id="3ca66-110">Exemplo 1: Atualizar um recurso ACS existente para ter marcas</span><span class="sxs-lookup"><span data-stu-id="3ca66-110">Example 1: Update an existing ACS resource to have tags</span></span>
```powershell
PS C:\> Update-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Tag @{ExampleKey1="ExampleValue1"}

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="3ca66-111">Anexa as marcas determinadas ao recurso ACS especificado.</span><span class="sxs-lookup"><span data-stu-id="3ca66-111">Attaches the given tags to the specified ACS resource.</span></span>

## <span data-ttu-id="3ca66-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3ca66-112">PARAMETERS</span></span>

### <span data-ttu-id="3ca66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca66-113">-DefaultProfile</span></span>
<span data-ttu-id="3ca66-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ca66-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ca66-115">-InputObject</span></span>
<span data-ttu-id="3ca66-116">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="3ca66-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ca66-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ca66-117">-Name</span></span>
<span data-ttu-id="3ca66-118">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3ca66-118">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="3ca66-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca66-119">-ResourceGroupName</span></span>
<span data-ttu-id="3ca66-120">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3ca66-120">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3ca66-121">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="3ca66-121">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3ca66-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ca66-122">-SubscriptionId</span></span>
<span data-ttu-id="3ca66-123">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca66-123">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3ca66-124">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3ca66-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3ca66-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ca66-125">-Tag</span></span>
<span data-ttu-id="3ca66-126">Marcas do serviço, que é uma lista de pares de valores-chave que descrevem o recurso.</span><span class="sxs-lookup"><span data-stu-id="3ca66-126">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="3ca66-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="3ca66-127">-Confirm</span></span>
<span data-ttu-id="3ca66-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca66-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca66-129">-WhatIf</span></span>
<span data-ttu-id="3ca66-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="3ca66-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca66-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ca66-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca66-132">CommonParameters</span></span>
<span data-ttu-id="3ca66-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca66-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ca66-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca66-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="3ca66-135">INPUTS</span></span>

### <span data-ttu-id="3ca66-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="3ca66-136">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="3ca66-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="3ca66-137">OUTPUTS</span></span>

### <span data-ttu-id="3ca66-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="3ca66-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="3ca66-139">Notas</span><span class="sxs-lookup"><span data-stu-id="3ca66-139">NOTES</span></span>

<span data-ttu-id="3ca66-140">Aliases</span><span class="sxs-lookup"><span data-stu-id="3ca66-140">ALIASES</span></span>

<span data-ttu-id="3ca66-141">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="3ca66-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ca66-142">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3ca66-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ca66-143">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3ca66-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ca66-144">INPUTOBJECT: <ICommunicationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="3ca66-144">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ca66-145">`[CommunicationServiceName <String>]`: o nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="3ca66-145">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="3ca66-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="3ca66-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ca66-147">`[Location <String>]`: A região do Azure</span><span class="sxs-lookup"><span data-stu-id="3ca66-147">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="3ca66-148">`[OperationId <String>]`: A ID de uma operação de assíncrona em andamento</span><span class="sxs-lookup"><span data-stu-id="3ca66-148">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="3ca66-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="3ca66-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3ca66-150">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="3ca66-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3ca66-151">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ca66-151">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3ca66-152">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3ca66-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3ca66-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ca66-153">RELATED LINKS</span></span>

