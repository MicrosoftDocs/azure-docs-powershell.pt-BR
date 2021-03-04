---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancereimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceReimage.md
ms.openlocfilehash: 644912b841475c660852adcda2cba320d9026618
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887018"
---
# <span data-ttu-id="93ae9-101">Invoke-AzCloudServiceRoleInstanceReimage</span><span class="sxs-lookup"><span data-stu-id="93ae9-101">Invoke-AzCloudServiceRoleInstanceReimage</span></span>

## <span data-ttu-id="93ae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="93ae9-103">A operação assíncrona da Instância de Função de Reimage reinstala o sistema operacional em instâncias de funções da Web ou funções de trabalho.</span><span class="sxs-lookup"><span data-stu-id="93ae9-103">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="93ae9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="93ae9-104">SYNTAX</span></span>

### <span data-ttu-id="93ae9-105">Reimage (Padrão)</span><span class="sxs-lookup"><span data-stu-id="93ae9-105">Reimage (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="93ae9-106">ReimageViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93ae9-106">ReimageViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceReimage -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="93ae9-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="93ae9-107">DESCRIPTION</span></span>
<span data-ttu-id="93ae9-108">A operação assíncrona da Instância de Função de Reimage reinstala o sistema operacional em instâncias de funções da Web ou funções de trabalho.</span><span class="sxs-lookup"><span data-stu-id="93ae9-108">The Reimage Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles.</span></span>

## <span data-ttu-id="93ae9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93ae9-109">EXAMPLES</span></span>

### <span data-ttu-id="93ae9-110">Exemplo 1: Instância da função Reimage de um serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="93ae9-110">Example 1: Reimage role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceReimage -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="93ae9-111">Este comando reimaja a instância de função chamada ContosoFrontEnd_IN_0 de serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="93ae9-111">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="93ae9-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="93ae9-112">PARAMETERS</span></span>

### <span data-ttu-id="93ae9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93ae9-113">-AsJob</span></span>
<span data-ttu-id="93ae9-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="93ae9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="93ae9-115">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="93ae9-115">-CloudServiceName</span></span>
<span data-ttu-id="93ae9-116">.</span><span class="sxs-lookup"><span data-stu-id="93ae9-116">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ae9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ae9-117">-DefaultProfile</span></span>
<span data-ttu-id="93ae9-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93ae9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93ae9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93ae9-119">-InputObject</span></span>
<span data-ttu-id="93ae9-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="93ae9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: ReimageViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93ae9-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="93ae9-121">-NoWait</span></span>
<span data-ttu-id="93ae9-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="93ae9-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="93ae9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93ae9-123">-PassThru</span></span>
<span data-ttu-id="93ae9-124">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="93ae9-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="93ae9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ae9-125">-ResourceGroupName</span></span>
<span data-ttu-id="93ae9-126">.</span><span class="sxs-lookup"><span data-stu-id="93ae9-126">.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ae9-127">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="93ae9-127">-RoleInstanceName</span></span>
<span data-ttu-id="93ae9-128">Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="93ae9-128">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ae9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93ae9-129">-SubscriptionId</span></span>
<span data-ttu-id="93ae9-130">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="93ae9-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="93ae9-131">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="93ae9-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reimage
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93ae9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93ae9-132">-Confirm</span></span>
<span data-ttu-id="93ae9-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93ae9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ae9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ae9-134">-WhatIf</span></span>
<span data-ttu-id="93ae9-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="93ae9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ae9-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="93ae9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ae9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ae9-137">CommonParameters</span></span>
<span data-ttu-id="93ae9-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ae9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ae9-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93ae9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ae9-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93ae9-140">INPUTS</span></span>

### <span data-ttu-id="93ae9-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="93ae9-141">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="93ae9-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="93ae9-142">OUTPUTS</span></span>

### <span data-ttu-id="93ae9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93ae9-143">System.Boolean</span></span>

## <span data-ttu-id="93ae9-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="93ae9-144">NOTES</span></span>

<span data-ttu-id="93ae9-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="93ae9-145">ALIASES</span></span>

<span data-ttu-id="93ae9-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="93ae9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="93ae9-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="93ae9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93ae9-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93ae9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="93ae9-149">INPUTOBJECT <ICloudServiceIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="93ae9-149">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93ae9-150">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="93ae9-150">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="93ae9-151">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="93ae9-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93ae9-152">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="93ae9-152">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="93ae9-153">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="93ae9-153">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="93ae9-154">`[RoleName <String>]`: Nome da função.</span><span class="sxs-lookup"><span data-stu-id="93ae9-154">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="93ae9-155">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="93ae9-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="93ae9-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="93ae9-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="93ae9-157">`[UpdateDomain <Int32?>]`: Especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="93ae9-157">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="93ae9-158">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="93ae9-158">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="93ae9-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93ae9-159">RELATED LINKS</span></span>

