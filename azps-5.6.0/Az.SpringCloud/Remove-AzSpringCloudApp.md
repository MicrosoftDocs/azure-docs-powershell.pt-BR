---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: c6dccbaa5e398d5d00b02a28cc8942b9e5264859
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888606"
---
# <span data-ttu-id="d8d09-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="d8d09-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="d8d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d09-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d09-103">Operação para excluir um Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8d09-103">Operation to delete an App.</span></span>

## <span data-ttu-id="d8d09-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d8d09-104">SYNTAX</span></span>

### <span data-ttu-id="d8d09-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d8d09-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d8d09-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d8d09-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8d09-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8d09-107">DESCRIPTION</span></span>
<span data-ttu-id="d8d09-108">Operação para excluir um Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8d09-108">Operation to delete an App.</span></span>

## <span data-ttu-id="d8d09-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8d09-109">EXAMPLES</span></span>

### <span data-ttu-id="d8d09-110">Exemplo 1: Remover o Aplicativo de Nuvem de Primavera pelo nome.</span><span class="sxs-lookup"><span data-stu-id="d8d09-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="d8d09-111">Remove Spring Cloud App pelo nome.</span><span class="sxs-lookup"><span data-stu-id="d8d09-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="d8d09-112">Exemplo 2: Remover o Aplicativo de Nuvem de Mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="d8d09-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="d8d09-113">Remover o Aplicativo de Nuvem de Mola do pipe.</span><span class="sxs-lookup"><span data-stu-id="d8d09-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="d8d09-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d8d09-114">PARAMETERS</span></span>

### <span data-ttu-id="d8d09-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8d09-115">-AsJob</span></span>
<span data-ttu-id="d8d09-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d8d09-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d8d09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d09-117">-DefaultProfile</span></span>
<span data-ttu-id="d8d09-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d09-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8d09-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8d09-119">-InputObject</span></span>
<span data-ttu-id="d8d09-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="d8d09-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d8d09-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d8d09-121">-Name</span></span>
<span data-ttu-id="d8d09-122">O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="d8d09-122">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d09-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d8d09-123">-NoWait</span></span>
<span data-ttu-id="d8d09-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d8d09-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d8d09-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8d09-125">-PassThru</span></span>
<span data-ttu-id="d8d09-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d8d09-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d8d09-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d09-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8d09-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d8d09-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d8d09-129">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="d8d09-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d8d09-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d8d09-130">-ServiceName</span></span>
<span data-ttu-id="d8d09-131">O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="d8d09-131">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d8d09-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d8d09-132">-SubscriptionId</span></span>
<span data-ttu-id="d8d09-133">Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d09-133">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d8d09-134">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d8d09-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d8d09-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8d09-135">-Confirm</span></span>
<span data-ttu-id="d8d09-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8d09-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8d09-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8d09-137">-WhatIf</span></span>
<span data-ttu-id="d8d09-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8d09-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8d09-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8d09-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8d09-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d09-140">CommonParameters</span></span>
<span data-ttu-id="d8d09-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8d09-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d09-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8d09-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d09-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8d09-143">INPUTS</span></span>

### <span data-ttu-id="d8d09-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d8d09-144">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d8d09-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d8d09-145">OUTPUTS</span></span>

### <span data-ttu-id="d8d09-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8d09-146">System.Boolean</span></span>

## <span data-ttu-id="d8d09-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="d8d09-147">NOTES</span></span>

<span data-ttu-id="d8d09-148">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d8d09-148">ALIASES</span></span>

<span data-ttu-id="d8d09-149">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="d8d09-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d8d09-150">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d8d09-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d8d09-151">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d8d09-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d8d09-152">INPUTOBJECT <ISpringCloudIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="d8d09-152">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d8d09-153">`[AppName <String>]`: O nome do recurso App.</span><span class="sxs-lookup"><span data-stu-id="d8d09-153">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d8d09-154">`[BindingName <String>]`: O nome do recurso Binding.</span><span class="sxs-lookup"><span data-stu-id="d8d09-154">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d8d09-155">`[CertificateName <String>]`: O nome do recurso de certificado.</span><span class="sxs-lookup"><span data-stu-id="d8d09-155">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d8d09-156">`[DeploymentName <String>]`: O nome do recurso Deployment.</span><span class="sxs-lookup"><span data-stu-id="d8d09-156">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d8d09-157">`[DomainName <String>]`: O nome do recurso de domínio personalizado.</span><span class="sxs-lookup"><span data-stu-id="d8d09-157">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d8d09-158">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="d8d09-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d8d09-159">`[Location <String>]`: a região</span><span class="sxs-lookup"><span data-stu-id="d8d09-159">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d8d09-160">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="d8d09-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d8d09-161">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="d8d09-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d8d09-162">`[ServiceName <String>]`: O nome do recurso Service.</span><span class="sxs-lookup"><span data-stu-id="d8d09-162">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d8d09-163">`[SubscriptionId <String>]`: Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d8d09-163">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d8d09-164">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d8d09-164">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d8d09-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8d09-165">RELATED LINKS</span></span>

