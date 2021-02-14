---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/new-azcommunicationservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/New-AzCommunicationServiceKey.md
ms.openlocfilehash: b97b0d640b00e2aa3b75d829464f8ebe7dd4f6d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111166"
---
# <span data-ttu-id="a3d33-101">New-AzCommunicationServiceKey</span><span class="sxs-lookup"><span data-stu-id="a3d33-101">New-AzCommunicationServiceKey</span></span>

## <span data-ttu-id="a3d33-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3d33-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d33-103">Regenerar a tecla de acesso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="a3d33-103">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="a3d33-104">PrimaryKey e SecondaryKey não podem ser regenerados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a3d33-104">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="a3d33-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3d33-105">SYNTAX</span></span>

### <span data-ttu-id="a3d33-106">RegenerateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3d33-106">RegenerateExpanded (Default)</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyType <KeyType>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a3d33-107">Regenerar</span><span class="sxs-lookup"><span data-stu-id="a3d33-107">Regenerate</span></span>
```
New-AzCommunicationServiceKey -CommunicationServiceName <String> -ResourceGroupName <String>
 -Parameter <IRegenerateKeyParameters> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3d33-108">RegenerateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a3d33-108">RegenerateViaIdentity</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> -Parameter <IRegenerateKeyParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a3d33-109">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a3d33-109">RegenerateViaIdentityExpanded</span></span>
```
New-AzCommunicationServiceKey -InputObject <ICommunicationIdentity> [-KeyType <KeyType>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a3d33-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3d33-110">DESCRIPTION</span></span>
<span data-ttu-id="a3d33-111">Regenerar a tecla de acesso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="a3d33-111">Regenerate CommunicationService access key.</span></span>
<span data-ttu-id="a3d33-112">PrimaryKey e SecondaryKey não podem ser regenerados ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a3d33-112">PrimaryKey and SecondaryKey cannot be regenerated at the same time.</span></span>

## <span data-ttu-id="a3d33-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3d33-113">EXAMPLES</span></span>

### <span data-ttu-id="a3d33-114">Exemplo 1: regenera a chave primária usando uma hashtable IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="a3d33-114">Example 1: Regenerates the Primary key using a IRegenerateKeyParameters hashtable</span></span>
```powershell
PS > New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -Parameter @{KeyType="Primary"}

PrimaryConnectionString              PrimaryKey
-----------------------              ----------
endpoint=<example-primary-endpoint>  <example-primarykey>
```

<span data-ttu-id="a3d33-115">Invalida a chave primária anterior, regenera uma nova e a retorna.</span><span class="sxs-lookup"><span data-stu-id="a3d33-115">Invalidates the previous Primary key, regenerate a new one and return it.</span></span>

### <span data-ttu-id="a3d33-116">Exemplo 2: regenera a chave secundária usando um Tipo-chave</span><span class="sxs-lookup"><span data-stu-id="a3d33-116">Example 2: Regenerates the Secondary key using a KeyType</span></span>
```powershell
PS C:\> New-AzCommunicationServiceKey -CommunicationServiceName ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1 -KeyType Secondary

SecondaryConnectionString               SecondaryKey
-----------------------                 ----------
endpoint=<example-secondary-endpoint>   <example-secondarykey>
```

<span data-ttu-id="a3d33-117">Invalida a chave Secundária anterior, regenera uma nova e a retorna.</span><span class="sxs-lookup"><span data-stu-id="a3d33-117">Invalidates the previous Secondary key, regenerate a new one and return it.</span></span>

## <span data-ttu-id="a3d33-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3d33-118">PARAMETERS</span></span>

### <span data-ttu-id="a3d33-119">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="a3d33-119">-CommunicationServiceName</span></span>
<span data-ttu-id="a3d33-120">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="a3d33-120">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="a3d33-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d33-121">-DefaultProfile</span></span>
<span data-ttu-id="a3d33-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d33-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3d33-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3d33-123">-InputObject</span></span>
<span data-ttu-id="a3d33-124">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a3d33-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3d33-125">-KeyType</span><span class="sxs-lookup"><span data-stu-id="a3d33-125">-KeyType</span></span>
<span data-ttu-id="a3d33-126">O tipo-chave a ser regenerado.</span><span class="sxs-lookup"><span data-stu-id="a3d33-126">The keyType to regenerate.</span></span>
<span data-ttu-id="a3d33-127">Deve ser 'principal' ou 'secundário' (não maiúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="a3d33-127">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

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

### <span data-ttu-id="a3d33-128">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3d33-128">-Parameter</span></span>
<span data-ttu-id="a3d33-129">Os parâmetros descrevem a solicitação para regenerar as teclas de acesso Para construir, confira a seção ANOTAÇÕES das propriedades PARÂMETRO e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a3d33-129">Parameters describes the request to regenerate access keys To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="a3d33-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d33-130">-ResourceGroupName</span></span>
<span data-ttu-id="a3d33-131">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a3d33-131">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a3d33-132">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="a3d33-132">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a3d33-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a3d33-133">-SubscriptionId</span></span>
<span data-ttu-id="a3d33-134">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d33-134">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a3d33-135">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a3d33-135">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a3d33-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a3d33-136">-Confirm</span></span>
<span data-ttu-id="a3d33-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3d33-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d33-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d33-138">-WhatIf</span></span>
<span data-ttu-id="a3d33-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a3d33-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3d33-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3d33-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d33-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d33-141">CommonParameters</span></span>
<span data-ttu-id="a3d33-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d33-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d33-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3d33-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d33-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="a3d33-144">INPUTS</span></span>

### <span data-ttu-id="a3d33-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span><span class="sxs-lookup"><span data-stu-id="a3d33-145">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.IRegenerateKeyParameters</span></span>

### <span data-ttu-id="a3d33-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="a3d33-146">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="a3d33-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="a3d33-147">OUTPUTS</span></span>

### <span data-ttu-id="a3d33-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span><span class="sxs-lookup"><span data-stu-id="a3d33-148">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ICommunicationServiceKeys</span></span>

## <span data-ttu-id="a3d33-149">Notas</span><span class="sxs-lookup"><span data-stu-id="a3d33-149">NOTES</span></span>

<span data-ttu-id="a3d33-150">Aliases</span><span class="sxs-lookup"><span data-stu-id="a3d33-150">ALIASES</span></span>

<span data-ttu-id="a3d33-151">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a3d33-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a3d33-152">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a3d33-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a3d33-153">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a3d33-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a3d33-154">INPUTOBJECT: <ICommunicationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a3d33-154">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a3d33-155">`[CommunicationServiceName <String>]`: o nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="a3d33-155">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="a3d33-156">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a3d33-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a3d33-157">`[Location <String>]`: A região do Azure</span><span class="sxs-lookup"><span data-stu-id="a3d33-157">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="a3d33-158">`[OperationId <String>]`: A ID de uma operação de assíncrona em andamento</span><span class="sxs-lookup"><span data-stu-id="a3d33-158">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="a3d33-159">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="a3d33-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a3d33-160">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="a3d33-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a3d33-161">`[SubscriptionId <String>]`: obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d33-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="a3d33-162">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a3d33-162">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="a3d33-163">PARÂMETRO: <IRegenerateKeyParameters> Os parâmetros descrevem a solicitação para regenerar as teclas de acesso</span><span class="sxs-lookup"><span data-stu-id="a3d33-163">PARAMETER <IRegenerateKeyParameters>: Parameters describes the request to regenerate access keys</span></span>
  - <span data-ttu-id="a3d33-164">`[KeyType <KeyType?>]`: o tipo-chave a ser regenerado.</span><span class="sxs-lookup"><span data-stu-id="a3d33-164">`[KeyType <KeyType?>]`: The keyType to regenerate.</span></span> <span data-ttu-id="a3d33-165">Deve ser 'principal' ou 'secundário' (não maiúsculas de minúsculas).</span><span class="sxs-lookup"><span data-stu-id="a3d33-165">Must be either 'primary' or 'secondary'(case-insensitive).</span></span>

## <span data-ttu-id="a3d33-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3d33-166">RELATED LINKS</span></span>

