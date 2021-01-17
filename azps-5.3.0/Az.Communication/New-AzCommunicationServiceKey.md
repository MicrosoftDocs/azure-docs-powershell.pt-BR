---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430282"
---
# <span data-ttu-id="91c77-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="91c77-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="91c77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91c77-102">SYNOPSIS</span></span>
<span data-ttu-id="91c77-103">Regenerar a chave de acesso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="91c77-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="91c77-104">PrimaryKey e SecondaryKey não podem ser regenerados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="91c77-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="91c77-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91c77-105">SYNTAX</span></span>

### <span data-ttu-id="91c77-106">RegenerateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="91c77-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="91c77-107">Reproduza</span><span class="sxs-lookup"><span data-stu-id="91c77-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="91c77-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="91c77-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="91c77-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="91c77-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="91c77-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91c77-110">DESCRIPTION</span></span>
<span data-ttu-id="91c77-111">Regenerar a chave de acesso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="91c77-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="91c77-112">PrimaryKey e SecondaryKey não podem ser regenerados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="91c77-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="91c77-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91c77-113">EXAMPLES</span></span>

### <span data-ttu-id="91c77-114">Exemplo 1: regenera a chave primária usando uma Hashtable IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="91c77-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="91c77-115">Invalida a chave primária anterior, regenea uma nova e a retorne.</span><span class="sxs-lookup"><span data-stu-id="91c77-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="91c77-116">Exemplo 2: regenera a chave secundária usando um KeyType</span><span class="sxs-lookup"><span data-stu-id="91c77-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="91c77-117">Invalida a chave secundária anterior, regenea uma nova e a retorne.</span><span class="sxs-lookup"><span data-stu-id="91c77-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="91c77-118">OS</span><span class="sxs-lookup"><span data-stu-id="91c77-118">PARAMETERS</span></span>

### <span data-ttu-id="91c77-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="91c77-119">-CommunicationServiceName</span></span>
<span data-ttu-id="91c77-120">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="91c77-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c77-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c77-121">-DefaultProfile</span></span>
<span data-ttu-id="91c77-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91c77-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c77-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91c77-123">-InputObject</span></span>
<span data-ttu-id="91c77-124">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="91c77-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: RegenerateViaIdentity, RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91c77-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="91c77-125">-KeyType</span></span>
<span data-ttu-id="91c77-126">O KeyType a ser regerado.</span><span class="sxs-lookup"><span data-stu-id="91c77-126">The keyType to regenerate.</span></span>
<span data-ttu-id="91c77-127">Deve ser ' Primary ' ou ' Secondary ' (não diferencia maiúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="91c77-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Support.KeyType
Parameter Sets: RegenerateExpanded, RegenerateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c77-128">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="91c77-128">-Parameter</span></span>
<span data-ttu-id="91c77-129">Parâmetros descreve a solicitação para gerar novamente as chaves de acesso a serem construídas, consulte a seção observações para propriedades de parâmetro e criar uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="91c77-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters
Parameter Sets: Regenerate, RegenerateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91c77-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c77-130">-ResourceGroupName</span></span>
<span data-ttu-id="91c77-131">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="91c77-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="91c77-132">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="91c77-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c77-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91c77-133">-SubscriptionId</span></span>
<span data-ttu-id="91c77-134">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="91c77-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="91c77-135">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="91c77-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Regenerate, RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91c77-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="91c77-136">-Confirm</span></span>
<span data-ttu-id="91c77-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91c77-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c77-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c77-138">-WhatIf</span></span>
<span data-ttu-id="91c77-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="91c77-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91c77-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91c77-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c77-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c77-141">CommonParameters</span></span>
<span data-ttu-id="91c77-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c77-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c77-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91c77-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c77-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91c77-144">INPUTS</span></span>

### <span data-ttu-id="91c77-145">Microsoft. Azure. PowerShell. cmdlets. Communication. Models. Api20200820Preview. IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="91c77-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="91c77-146">Microsoft. Azure. PowerShell. cmdlets. Communication. Models. ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="91c77-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="91c77-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91c77-147">OUTPUTS</span></span>

### <span data-ttu-id="91c77-148">Microsoft. Azure. PowerShell. cmdlets. Communication. Models. Api20200820Preview. ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="91c77-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="91c77-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91c77-149">NOTES</span></span>

<span data-ttu-id="91c77-150">ALIASES</span><span class="sxs-lookup"><span data-stu-id="91c77-150">ALIASES</span></span>

<span data-ttu-id="91c77-151">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="91c77-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91c77-152">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="91c77-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91c77-153">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91c77-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91c77-154">INPUTobject <ICommunicationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="91c77-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91c77-155">`[CommunicationServiceName <String>]`: O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="91c77-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="91c77-156">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="91c77-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91c77-157">`[Location <String>]`: A região do Azure</span><span class="sxs-lookup"><span data-stu-id="91c77-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="91c77-158">`[OperationId <String>]`: A ID de uma operação assíncrona em andamento</span><span class="sxs-lookup"><span data-stu-id="91c77-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="91c77-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="91c77-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="91c77-160">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="91c77-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="91c77-161">`[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="91c77-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="91c77-162">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="91c77-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="91c77-163">PARÂMETRO <IRegenerateKeyParameters> : parâmetros descreve a solicitação para regenerar as teclas de acesso</span><span class="sxs-lookup"><span data-stu-id="91c77-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="91c77-164">`[KeyType <KeyType?>]`: O KeyType a ser regerado.</span><span class="sxs-lookup"><span data-stu-id="91c77-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="91c77-165">Deve ser ' Primary ' ou ' Secondary ' (não diferencia maiúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="91c77-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="91c77-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91c77-166">RELATED LINKS</span></span>

