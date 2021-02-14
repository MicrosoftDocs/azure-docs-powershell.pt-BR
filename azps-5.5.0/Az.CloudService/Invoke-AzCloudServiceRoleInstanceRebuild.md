---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/invoke-azcloudserviceroleinstancerebuild
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Invoke-AzCloudServiceRoleInstanceRebuild.md
ms.openlocfilehash: d998e29fc254b1bf507ab7d7732bc3bdcf68f54b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111170"
---
# <span data-ttu-id="d5b4b-101">Invoke-AzCloudServiceRoleInstanceRebuild</span><span class="sxs-lookup"><span data-stu-id="d5b4b-101">Invoke-AzCloudServiceRoleInstanceRebuild</span></span>

## <span data-ttu-id="d5b4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b4b-103">A operação assíncrona Recriar Instância de Função reinstala o sistema operacional em instâncias de funções da Web ou funções de trabalhador e inicializa os recursos de armazenamento usados por eles.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-103">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="d5b4b-104">Se você não quiser inicializar recursos de armazenamento, poderá usar a Instância de Função de Reimage.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-104">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="d5b4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5b4b-105">SYNTAX</span></span>

### <span data-ttu-id="d5b4b-106">Recriar (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d5b4b-106">Rebuild (Default)</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d5b4b-107">RebuildViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d5b4b-107">RebuildViaIdentity</span></span>
```
Invoke-AzCloudServiceRoleInstanceRebuild -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5b4b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5b4b-108">DESCRIPTION</span></span>
<span data-ttu-id="d5b4b-109">A operação assíncrona Recriar Instância de Função reinstala o sistema operacional em instâncias de funções da Web ou funções de trabalhador e inicializa os recursos de armazenamento usados por eles.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-109">The Rebuild Role Instance asynchronous operation reinstalls the operating system on instances of web roles or worker roles and initializes the storage resources that are used by them.</span></span>
<span data-ttu-id="d5b4b-110">Se você não quiser inicializar recursos de armazenamento, poderá usar a Instância de Função de Reimage.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-110">If you do not want to initialize storage resources, you can use Reimage Role Instance.</span></span>

## <span data-ttu-id="d5b4b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d5b4b-111">EXAMPLES</span></span>

### <span data-ttu-id="d5b4b-112">Exemplo 1: Recriar instância de função de um serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="d5b4b-112">Example 1: Rebuild role instance of a cloud service</span></span>
```powershell
PS C:\> Invoke-AzCloudServiceRoleInstanceRebuild -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"
```

<span data-ttu-id="d5b4b-113">Esse comando reima instância de função chamada ContosoFrontEnd_IN_0 de serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-113">This command reimages role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="d5b4b-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5b4b-114">PARAMETERS</span></span>

### <span data-ttu-id="d5b4b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5b4b-115">-AsJob</span></span>
<span data-ttu-id="d5b4b-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d5b4b-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d5b4b-117">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="d5b4b-117">-CloudServiceName</span></span>
<span data-ttu-id="d5b4b-118">.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-118">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b4b-119">-DefaultProfile</span></span>
<span data-ttu-id="d5b4b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5b4b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5b4b-121">-InputObject</span></span>
<span data-ttu-id="d5b4b-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: RebuildViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d5b4b-123">-NoWait</span></span>
<span data-ttu-id="d5b4b-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="d5b4b-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d5b4b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5b4b-125">-PassThru</span></span>
<span data-ttu-id="d5b4b-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="d5b4b-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d5b4b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5b4b-127">-ResourceGroupName</span></span>
<span data-ttu-id="d5b4b-128">.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-128">.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4b-129">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="d5b4b-129">-RoleInstanceName</span></span>
<span data-ttu-id="d5b4b-130">Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-130">Name of the role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5b4b-131">-SubscriptionId</span></span>
<span data-ttu-id="d5b4b-132">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5b4b-133">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Rebuild
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b4b-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d5b4b-134">-Confirm</span></span>
<span data-ttu-id="d5b4b-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b4b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5b4b-136">-WhatIf</span></span>
<span data-ttu-id="d5b4b-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5b4b-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b4b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b4b-139">CommonParameters</span></span>
<span data-ttu-id="d5b4b-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b4b-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5b4b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b4b-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="d5b4b-142">INPUTS</span></span>

### <span data-ttu-id="d5b4b-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="d5b4b-143">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="d5b4b-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="d5b4b-144">OUTPUTS</span></span>

### <span data-ttu-id="d5b4b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5b4b-145">System.Boolean</span></span>

## <span data-ttu-id="d5b4b-146">Notas</span><span class="sxs-lookup"><span data-stu-id="d5b4b-146">NOTES</span></span>

<span data-ttu-id="d5b4b-147">Aliases</span><span class="sxs-lookup"><span data-stu-id="d5b4b-147">ALIASES</span></span>

<span data-ttu-id="d5b4b-148">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="d5b4b-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5b4b-149">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5b4b-150">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5b4b-151">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="d5b4b-151">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5b4b-152">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d5b4b-152">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="d5b4b-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="d5b4b-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5b4b-154">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="d5b4b-154">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="d5b4b-155">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-155">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="d5b4b-156">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-156">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="d5b4b-157">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-157">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d5b4b-158">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d5b4b-159">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-159">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="d5b4b-160">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d5b4b-160">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="d5b4b-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5b4b-161">RELATED LINKS</span></span>

