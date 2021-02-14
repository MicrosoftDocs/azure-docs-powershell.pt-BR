---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/remove-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Remove-AzCommunicationService.md
ms.openlocfilehash: c165f9d69b18631f53bdc9444a623f43599532fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111165"
---
# <span data-ttu-id="98542-101">Remove-AzCommunicationService</span><span class="sxs-lookup"><span data-stu-id="98542-101">Remove-AzCommunicationService</span></span>

## <span data-ttu-id="98542-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98542-102">SYNOPSIS</span></span>
<span data-ttu-id="98542-103">Operação para excluir um CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="98542-103">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="98542-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98542-104">SYNTAX</span></span>

### <span data-ttu-id="98542-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="98542-105">Delete (Default)</span></span>
```
Remove-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98542-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="98542-106">DeleteViaIdentity</span></span>
```
Remove-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98542-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="98542-107">DESCRIPTION</span></span>
<span data-ttu-id="98542-108">Operação para excluir um CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="98542-108">Operation to delete a CommunicationService.</span></span>

## <span data-ttu-id="98542-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="98542-109">EXAMPLES</span></span>

### <span data-ttu-id="98542-110">Exemplo 1: Remover o recurso de Comunicação do Azure especificado</span><span class="sxs-lookup"><span data-stu-id="98542-110">Example 1: Remove the specified Azure Communication resource</span></span>
```powershell
PS C:\> Remove-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1
```

<span data-ttu-id="98542-111">Remover/excluir o recurso comunicação do Azure.</span><span class="sxs-lookup"><span data-stu-id="98542-111">Remove / Delete the Azure Communication resource.</span></span>

## <span data-ttu-id="98542-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98542-112">PARAMETERS</span></span>

### <span data-ttu-id="98542-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98542-113">-AsJob</span></span>
<span data-ttu-id="98542-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="98542-114">Run the command as a job</span></span>

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

### <span data-ttu-id="98542-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98542-115">-DefaultProfile</span></span>
<span data-ttu-id="98542-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98542-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98542-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98542-117">-InputObject</span></span>
<span data-ttu-id="98542-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="98542-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98542-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="98542-119">-Name</span></span>
<span data-ttu-id="98542-120">O nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="98542-120">The name of the CommunicationService resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98542-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="98542-121">-NoWait</span></span>
<span data-ttu-id="98542-122">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="98542-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="98542-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98542-123">-PassThru</span></span>
<span data-ttu-id="98542-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="98542-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="98542-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98542-125">-ResourceGroupName</span></span>
<span data-ttu-id="98542-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="98542-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="98542-127">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="98542-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98542-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98542-128">-SubscriptionId</span></span>
<span data-ttu-id="98542-129">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="98542-129">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="98542-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="98542-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98542-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="98542-131">-Confirm</span></span>
<span data-ttu-id="98542-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98542-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98542-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98542-133">-WhatIf</span></span>
<span data-ttu-id="98542-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="98542-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98542-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98542-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98542-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98542-136">CommonParameters</span></span>
<span data-ttu-id="98542-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98542-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98542-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98542-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98542-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="98542-139">INPUTS</span></span>

### <span data-ttu-id="98542-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span><span class="sxs-lookup"><span data-stu-id="98542-140">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity</span></span>

## <span data-ttu-id="98542-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="98542-141">OUTPUTS</span></span>

### <span data-ttu-id="98542-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98542-142">System.Boolean</span></span>

## <span data-ttu-id="98542-143">Notas</span><span class="sxs-lookup"><span data-stu-id="98542-143">NOTES</span></span>

<span data-ttu-id="98542-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="98542-144">ALIASES</span></span>

<span data-ttu-id="98542-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="98542-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="98542-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="98542-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="98542-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="98542-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="98542-148">INPUTOBJECT: <ICommunicationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="98542-148">INPUTOBJECT <ICommunicationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="98542-149">`[CommunicationServiceName <String>]`: o nome do recurso CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="98542-149">`[CommunicationServiceName <String>]`: The name of the CommunicationService resource.</span></span>
  - <span data-ttu-id="98542-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="98542-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="98542-151">`[Location <String>]`: A região do Azure</span><span class="sxs-lookup"><span data-stu-id="98542-151">`[Location <String>]`: The Azure region</span></span>
  - <span data-ttu-id="98542-152">`[OperationId <String>]`: A ID de uma operação de assíncrona em andamento</span><span class="sxs-lookup"><span data-stu-id="98542-152">`[OperationId <String>]`: The ID of an ongoing async operation</span></span>
  - <span data-ttu-id="98542-153">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="98542-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="98542-154">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="98542-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="98542-155">`[SubscriptionId <String>]`: obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="98542-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="98542-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="98542-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="98542-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98542-157">RELATED LINKS</span></span>

