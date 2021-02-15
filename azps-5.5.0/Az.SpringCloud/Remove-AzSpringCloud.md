---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116164"
---
# <span data-ttu-id="8a542-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="8a542-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="8a542-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a542-102">SYNOPSIS</span></span>
<span data-ttu-id="8a542-103">Operação para excluir um Serviço.</span><span class="sxs-lookup"><span data-stu-id="8a542-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="8a542-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a542-104">SYNTAX</span></span>

### <span data-ttu-id="8a542-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8a542-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8a542-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a542-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8a542-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a542-107">DESCRIPTION</span></span>
<span data-ttu-id="8a542-108">Operação para excluir um Serviço.</span><span class="sxs-lookup"><span data-stu-id="8a542-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="8a542-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a542-109">EXAMPLES</span></span>

### <span data-ttu-id="8a542-110">Exemplo 1: Remover o Serviço de Nuvem de Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="8a542-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="8a542-111">Remover o Serviço de Nuvem de Primavera por nome.</span><span class="sxs-lookup"><span data-stu-id="8a542-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="8a542-112">Exemplo 2: Remover o Serviço de Nuvem de Primavera do cano.</span><span class="sxs-lookup"><span data-stu-id="8a542-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="8a542-113">Remover o Serviço de Nuvem de Primavera do cano.</span><span class="sxs-lookup"><span data-stu-id="8a542-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="8a542-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a542-114">PARAMETERS</span></span>

### <span data-ttu-id="8a542-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a542-115">-AsJob</span></span>
<span data-ttu-id="8a542-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8a542-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8a542-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a542-117">-DefaultProfile</span></span>
<span data-ttu-id="8a542-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a542-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a542-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a542-119">-InputObject</span></span>
<span data-ttu-id="8a542-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8a542-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a542-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a542-121">-Name</span></span>
<span data-ttu-id="8a542-122">O nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="8a542-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a542-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8a542-123">-NoWait</span></span>
<span data-ttu-id="8a542-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="8a542-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8a542-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a542-125">-PassThru</span></span>
<span data-ttu-id="8a542-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8a542-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8a542-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a542-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a542-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="8a542-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8a542-129">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="8a542-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8a542-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a542-130">-SubscriptionId</span></span>
<span data-ttu-id="8a542-131">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a542-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8a542-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8a542-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8a542-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8a542-133">-Confirm</span></span>
<span data-ttu-id="8a542-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a542-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a542-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a542-135">-WhatIf</span></span>
<span data-ttu-id="8a542-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8a542-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a542-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a542-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a542-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a542-138">CommonParameters</span></span>
<span data-ttu-id="8a542-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a542-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a542-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a542-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a542-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="8a542-141">INPUTS</span></span>

### <span data-ttu-id="8a542-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="8a542-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="8a542-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="8a542-143">OUTPUTS</span></span>

### <span data-ttu-id="8a542-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a542-144">System.Boolean</span></span>

## <span data-ttu-id="8a542-145">Notas</span><span class="sxs-lookup"><span data-stu-id="8a542-145">NOTES</span></span>

<span data-ttu-id="8a542-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="8a542-146">ALIASES</span></span>

<span data-ttu-id="8a542-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="8a542-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8a542-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8a542-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a542-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8a542-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8a542-150">INPUTOBJECT: <ISpringCloudIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="8a542-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a542-151">`[AppName <String>]`: o nome do recurso Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8a542-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="8a542-152">`[BindingName <String>]`: o nome do recurso Encadernação.</span><span class="sxs-lookup"><span data-stu-id="8a542-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="8a542-153">`[CertificateName <String>]`: o nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="8a542-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="8a542-154">`[DeploymentName <String>]`: o nome do recurso implantação.</span><span class="sxs-lookup"><span data-stu-id="8a542-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="8a542-155">`[DomainName <String>]`: o nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="8a542-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="8a542-156">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="8a542-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a542-157">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="8a542-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="8a542-158">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="8a542-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8a542-159">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="8a542-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8a542-160">`[ServiceName <String>]`: o nome do recurso Serviço.</span><span class="sxs-lookup"><span data-stu-id="8a542-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="8a542-161">`[SubscriptionId <String>]`: obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8a542-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8a542-162">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="8a542-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8a542-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a542-163">RELATED LINKS</span></span>

