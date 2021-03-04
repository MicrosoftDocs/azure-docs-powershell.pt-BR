---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: f9f4cc86a07c50718511c3ed0889d96f7acec9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890475"
---
# <span data-ttu-id="d274c-101">Get-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="d274c-101">Get-AzCommunicationService</span></span>

## <span data-ttu-id="d274c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d274c-102">SYNOPSIS</span></span>
<span data-ttu-id="d274c-103">Obter o CommunicationService e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d274c-103">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="d274c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d274c-104">SYNTAX</span></span>

### <span data-ttu-id="d274c-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d274c-105">List (Default)</span></span>
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d274c-106">Obter</span><span class="sxs-lookup"><span data-stu-id="d274c-106">Get</span></span>
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d274c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d274c-107">GetViaIdentity</span></span>
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d274c-108">List1</span><span class="sxs-lookup"><span data-stu-id="d274c-108">List1</span></span>
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d274c-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d274c-109">DESCRIPTION</span></span>
<span data-ttu-id="d274c-110">Obter o CommunicationService e suas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d274c-110">Get the CommunicationService and its properties.</span></span>

## <span data-ttu-id="d274c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d274c-111">EXAMPLES</span></span>

### <span data-ttu-id="d274c-112">Exemplo 1: Listar Serviços de Comunicação existentes para uma assinatura</span><span class="sxs-lookup"><span data-stu-id="d274c-112">Example 1: List existing CommunicationServices for a Subscription</span></span>
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

<span data-ttu-id="d274c-113">Retorna uma lista de todos os recursos do ACS sob essa assinatura.</span><span class="sxs-lookup"><span data-stu-id="d274c-113">Returns a list of all ACS resources under that subscription.</span></span>

### <span data-ttu-id="d274c-114">Exemplo 2: obter informações sobre o recurso de Comunicação do Azure especificado</span><span class="sxs-lookup"><span data-stu-id="d274c-114">Example 2: Get infomation on specified Azure Communication resource</span></span>
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

<span data-ttu-id="d274c-115">Retorna as informações sobre um recurso ACS, se um parâmetro fornecido correspondente for encontrado.</span><span class="sxs-lookup"><span data-stu-id="d274c-115">Returns the information on an ACS resource, if one matching provided parameters is found.</span></span>

## <span data-ttu-id="d274c-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d274c-116">PARAMETERS</span></span>

### <span data-ttu-id="d274c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d274c-117">-DefaultProfile</span></span>
<span data-ttu-id="d274c-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d274c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d274c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d274c-119">-InputObject</span></span>
<span data-ttu-id="d274c-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d274c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d274c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d274c-121">-Name</span></span>
<span data-ttu-id="d274c-122">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="d274c-122">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d274c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d274c-123">-ResourceGroupName</span></span>
<span data-ttu-id="d274c-124">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d274c-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d274c-125">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="d274c-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d274c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d274c-126">-SubscriptionId</span></span>
<span data-ttu-id="d274c-127">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d274c-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d274c-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d274c-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d274c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d274c-129">CommonParameters</span></span>
<span data-ttu-id="d274c-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d274c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d274c-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d274c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d274c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d274c-132">INPUTS</span></span>

### <span data-ttu-id="d274c-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="d274c-133">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="d274c-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d274c-134">OUTPUTS</span></span>

### <span data-ttu-id="d274c-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span><span class="sxs-lookup"><span data-stu-id="d274c-135">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceResource</span></span>

## <span data-ttu-id="d274c-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="d274c-136">NOTES</span></span>

<span data-ttu-id="d274c-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d274c-137">ALIASES</span></span>

<span data-ttu-id="d274c-138">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="d274c-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d274c-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d274c-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d274c-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d274c-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d274c-141">INPUTOBJECT <ICommunicationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="d274c-141">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d274c-142">`[CommunicationServiceName <String>]`: O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="d274c-142">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="d274c-143">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d274c-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d274c-144">`[Location <String>]`: A região do Azure</span><span class="sxs-lookup"><span data-stu-id="d274c-144">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="d274c-145">`[OperationId <String>]`: A ID de uma operação assíncrona em andamento</span><span class="sxs-lookup"><span data-stu-id="d274c-145">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="d274c-146">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d274c-146">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d274c-147">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="d274c-147">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d274c-148">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d274c-148">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d274c-149">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d274c-149">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d274c-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d274c-150">RELATED LINKS</span></span>

