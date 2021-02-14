---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/Switch-AzCloudService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Switch-AzCloudService.md
ms.openlocfilehash: f10d11dbbe98c098286a072d5882bf5d3a464d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115495"
---
# <span data-ttu-id="f76ee-101">Switch-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="f76ee-101">Switch-AzCloudService</span></span>

## <span data-ttu-id="f76ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f76ee-102">SYNOPSIS</span></span>
<span data-ttu-id="f76ee-103">Troca VIPs entre dois balanceadores de carga de serviço na nuvem (suporte estendido).</span><span class="sxs-lookup"><span data-stu-id="f76ee-103">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="f76ee-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f76ee-104">SYNTAX</span></span>

### <span data-ttu-id="f76ee-105">CloudServiceName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f76ee-105">CloudServiceName (Default)</span></span>
```
Switch-AzCloudService -CloudServiceName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Async] [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f76ee-106">CloudService</span><span class="sxs-lookup"><span data-stu-id="f76ee-106">CloudService</span></span>
```
Switch-AzCloudService -CloudService <CloudService> [-SubscriptionId <String>] [-Async]
 [-DefaultProfile <PSObject>] [-AsJob] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f76ee-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f76ee-107">DESCRIPTION</span></span>
<span data-ttu-id="f76ee-108">Troca VIPs entre dois balanceadores de carga de serviço na nuvem (suporte estendido).</span><span class="sxs-lookup"><span data-stu-id="f76ee-108">Swaps VIPs between two cloud service (extended support) load balancers.</span></span>

## <span data-ttu-id="f76ee-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f76ee-109">EXAMPLES</span></span>

### <span data-ttu-id="f76ee-110">Exemplo 1: Alternar o serviço de nuvem usando o nome</span><span class="sxs-lookup"><span data-stu-id="f76ee-110">Example 1: Switch cloud service using name</span></span>
```powershell
PS C:\> Switch-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca

```

<span data-ttu-id="f76ee-111">O comando Acima invocará a operação vipswap no serviço de Nuvem com o nome 'BService' e executará a operação assim que o usuário confirmar a ação no prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="f76ee-111">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="f76ee-112">'BService' com o serviço de nuvem permutável.</span><span class="sxs-lookup"><span data-stu-id="f76ee-112">'BService' with be swapped with its swappable cloud service.</span></span>

### <span data-ttu-id="f76ee-113">Exemplo 2: Alternar o serviço de nuvem usando o objeto de serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="f76ee-113">Example 2: Switch cloud service using cloud service object</span></span>
```powershell
PS C:\> $cs = Get-AzCloudService -ResourceGroupName "BRGThree" -CloudServiceName BService -SubscriptionId 1133e0eb-b53c-1234-b478-2eac8f04afca
PS C:\> Switch-AzCloudService -CloudService $cs

```

<span data-ttu-id="f76ee-114">O comando Acima invocará a operação vipswap no serviço de Nuvem com o nome 'BService' e executará a operação assim que o usuário confirmar a ação no prompt de confirmação.</span><span class="sxs-lookup"><span data-stu-id="f76ee-114">Above command invokes the vipswap operation on the Cloud service with name 'BService' and will perform the operation once the user confirms the action on the confirmation prompt.</span></span>
<span data-ttu-id="f76ee-115">'BService' com o serviço de nuvem permutável.</span><span class="sxs-lookup"><span data-stu-id="f76ee-115">'BService' with be swapped with its swappable cloud service.</span></span>

## <span data-ttu-id="f76ee-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f76ee-116">PARAMETERS</span></span>

### <span data-ttu-id="f76ee-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f76ee-117">-AsJob</span></span>
<span data-ttu-id="f76ee-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f76ee-118">Run the command as a job</span></span>

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

### <span data-ttu-id="f76ee-119">-Async</span><span class="sxs-lookup"><span data-stu-id="f76ee-119">-Async</span></span>


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

### <span data-ttu-id="f76ee-120">-CloudService</span><span class="sxs-lookup"><span data-stu-id="f76ee-120">-CloudService</span></span>
<span data-ttu-id="f76ee-121">Para construir, confira a seção ANOTAÇÕES para propriedades DE SERVIÇO NA NUVEM e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f76ee-121">To construct, see NOTES section for CLOUDSERVICE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudService
Parameter Sets: CloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f76ee-122">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="f76ee-122">-CloudServiceName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f76ee-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f76ee-123">-DefaultProfile</span></span>
<span data-ttu-id="f76ee-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f76ee-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f76ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f76ee-125">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: CloudServiceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f76ee-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f76ee-126">-SubscriptionId</span></span>
<span data-ttu-id="f76ee-127">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f76ee-127">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f76ee-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f76ee-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f76ee-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f76ee-129">-Confirm</span></span>
<span data-ttu-id="f76ee-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f76ee-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f76ee-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f76ee-131">-WhatIf</span></span>
<span data-ttu-id="f76ee-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f76ee-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f76ee-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f76ee-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f76ee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f76ee-134">CommonParameters</span></span>
<span data-ttu-id="f76ee-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f76ee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f76ee-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f76ee-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f76ee-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="f76ee-137">INPUTS</span></span>

## <span data-ttu-id="f76ee-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="f76ee-138">OUTPUTS</span></span>

### <span data-ttu-id="f76ee-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f76ee-139">System.Boolean</span></span>

## <span data-ttu-id="f76ee-140">Notas</span><span class="sxs-lookup"><span data-stu-id="f76ee-140">NOTES</span></span>

<span data-ttu-id="f76ee-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="f76ee-141">ALIASES</span></span>

<span data-ttu-id="f76ee-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f76ee-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f76ee-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f76ee-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f76ee-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f76ee-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f76ee-145">SERVIÇO DE <CloudService> NUVEM:</span><span class="sxs-lookup"><span data-stu-id="f76ee-145">CLOUDSERVICE <CloudService>:</span></span> 
  - <span data-ttu-id="f76ee-146">`Location <String>`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="f76ee-146">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="f76ee-147">`[Configuration <String>]`: especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-147">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="f76ee-148">`[ConfigurationUrl <String>]`: especifica uma URL que se refere ao local da configuração do serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="f76ee-148">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="f76ee-149">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f76ee-149">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="f76ee-150">Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="f76ee-150">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="f76ee-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: descreve um perfil de extensão de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-151">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="f76ee-152">`[Extension <IExtension[]>]`: Lista de extensões do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-152">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="f76ee-153">`[AutoUpgradeMinorVersion <Boolean?>]`: especifique explicitamente se a plataforma pode atualizar automaticamente o tipoHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="f76ee-153">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="f76ee-154">`[ForceUpdateTag <String>]`: Marque para forçar a aplicação das configurações públicas e protegidas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="f76ee-154">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="f76ee-155">Alterar o valor da marca permite executar a extensão de forma a executar a extensão sem alterar as configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="f76ee-155">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="f76ee-156">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="f76ee-156">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="f76ee-157">Se nem forçarUpdateTag nem nenhuma das configurações públicas ou protegidas mudar, a extensão fluiria para a instância de função com o mesmo número de sequência, e a implementação de manipuladores decidirá se a executará ou não.</span><span class="sxs-lookup"><span data-stu-id="f76ee-157">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="f76ee-158">`[Name <String>]`: o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-158">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="f76ee-159">`[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviar para a instância de função.</span><span class="sxs-lookup"><span data-stu-id="f76ee-159">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="f76ee-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f76ee-160">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="f76ee-161">`[Publisher <String>]`: o nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-161">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="f76ee-162">`[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-162">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="f76ee-163">Se a propriedade não for especificada ou '\*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-163">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="f76ee-164">`[Setting <String>]`: Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-164">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="f76ee-165">Para extensões JSON, essas são as configurações JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-165">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="f76ee-166">Para Extensão XML (como RDP), essa é a configuração XML para a extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-166">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="f76ee-167">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="f76ee-167">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f76ee-168">`[Type <String>]`: especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-168">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="f76ee-169">`[TypeHandlerVersion <String>]`: especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-169">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="f76ee-170">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="f76ee-170">Specifies the version of the extension.</span></span> <span data-ttu-id="f76ee-171">Se esse elemento não for especificado ou um asterisco (\*) for usado como valor, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="f76ee-171">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="f76ee-172">Se o valor for especificado com um número de versão principal e um asterisco como o número da versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada.</span><span class="sxs-lookup"><span data-stu-id="f76ee-172">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="f76ee-173">Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada.</span><span class="sxs-lookup"><span data-stu-id="f76ee-173">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="f76ee-174">Se uma versão for especificada, uma atualização automática será executada na instância da função.</span><span class="sxs-lookup"><span data-stu-id="f76ee-174">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="f76ee-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Perfil de Rede do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-175">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="f76ee-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: a lista de configurações de balanceador de carga para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-176">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="f76ee-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP</span><span class="sxs-lookup"><span data-stu-id="f76ee-177">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="f76ee-178">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="f76ee-178">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="f76ee-179">`[PrivateIPAddress <String>]`: O endereço IP particular referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-179">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="f76ee-180">`[PublicIPAddressId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="f76ee-180">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="f76ee-181">`[SubnetId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="f76ee-181">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f76ee-182">`[Name <String>]`: Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="f76ee-182">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="f76ee-183">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="f76ee-183">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="f76ee-184">`[Id <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="f76ee-184">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="f76ee-185">`[OSProfile <ICloudServiceOSProfile>]`: descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-185">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="f76ee-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: especifica o conjunto de certificados que devem ser instalados nas instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="f76ee-186">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="f76ee-187">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="f76ee-187">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="f76ee-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências do cofre-chave no SourceVault que contêm certificados.</span><span class="sxs-lookup"><span data-stu-id="f76ee-188">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="f76ee-189">`[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado para o Cofre de Chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="f76ee-189">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="f76ee-190">`[PackageUrl <String>]`: especifica uma URL que se refere ao local do pacote de serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="f76ee-190">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="f76ee-191">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f76ee-191">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="f76ee-192">Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="f76ee-192">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="f76ee-193">`[RoleProfile <ICloudServiceRoleProfile>]`: descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-193">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="f76ee-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-194">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="f76ee-195">`[Name <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="f76ee-195">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="f76ee-196">`[SkuCapacity <Int64?>]`: especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-196">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="f76ee-197">`[SkuName <String>]`: o nome da sKU.</span><span class="sxs-lookup"><span data-stu-id="f76ee-197">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="f76ee-198">OBSERVAÇÃO: se a nova SKU não for suportada no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para a SKU antiga.</span><span class="sxs-lookup"><span data-stu-id="f76ee-198">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="f76ee-199">`[SkuTier <String>]`: especifica o nível do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-199">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="f76ee-200">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="f76ee-200">Possible Values are</span></span> <br /><br /> <span data-ttu-id="f76ee-201">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="f76ee-201">**Standard**</span></span> <br /><br /> <span data-ttu-id="f76ee-202">**Basic**</span><span class="sxs-lookup"><span data-stu-id="f76ee-202">**Basic**</span></span>
  - <span data-ttu-id="f76ee-203">`[StartCloudService <Boolean?>]`: (Opcional) Indica se o serviço de nuvem deve ser iniciar imediatamente após sua criação.</span><span class="sxs-lookup"><span data-stu-id="f76ee-203">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="f76ee-204">O valor padrão é `true` .</span><span class="sxs-lookup"><span data-stu-id="f76ee-204">The default value is `true`.</span></span>         <span data-ttu-id="f76ee-205">Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f76ee-205">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="f76ee-206">Em vez disso, o serviço é PoweredOff até que você ligue para Iniciar, momento em que o serviço será iniciado.</span><span class="sxs-lookup"><span data-stu-id="f76ee-206">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="f76ee-207">Um serviço implantado ainda incorre em encargos, mesmo que ele esteja desligado.</span><span class="sxs-lookup"><span data-stu-id="f76ee-207">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="f76ee-208">`[Tag <ICloudServiceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="f76ee-208">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="f76ee-209">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="f76ee-209">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="f76ee-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Modo de atualização para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f76ee-210">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="f76ee-211">As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado.</span><span class="sxs-lookup"><span data-stu-id="f76ee-211">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="f76ee-212">As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização.</span><span class="sxs-lookup"><span data-stu-id="f76ee-212">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="f76ee-213">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="f76ee-213">Possible Values are</span></span> <br /><br /><span data-ttu-id="f76ee-214">**Automático**</span><span class="sxs-lookup"><span data-stu-id="f76ee-214">**Auto**</span></span><br /><br /><span data-ttu-id="f76ee-215">**Manual**</span><span class="sxs-lookup"><span data-stu-id="f76ee-215">**Manual**</span></span> <br /><br /><span data-ttu-id="f76ee-216">**Simultânea**</span><span class="sxs-lookup"><span data-stu-id="f76ee-216">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="f76ee-217">Se não especificado, o valor padrão será Automático. Se definido como Manual, PUT UpdateDomain deverá ser chamado para aplicar a atualização.</span><span class="sxs-lookup"><span data-stu-id="f76ee-217">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="f76ee-218">Se definido como Automático, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.</span><span class="sxs-lookup"><span data-stu-id="f76ee-218">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="f76ee-219">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f76ee-219">RELATED LINKS</span></span>

