---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/update-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Update-AzCloudService.md
ms.openlocfilehash: e0f9ad794f1631c5c8615480c6074f040f7fe749
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111169"
---
# <span data-ttu-id="b35fa-101">Update-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="b35fa-101">Update-AzCloudService</span></span>

## <span data-ttu-id="b35fa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b35fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b35fa-103">Criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-103">Create or update a cloud service.</span></span>
<span data-ttu-id="b35fa-104">Observe que algumas propriedades podem ser definidas somente durante a criação de serviços na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-104">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="b35fa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b35fa-105">SYNTAX</span></span>

```
Update-AzCloudService -InputObject <ICloudServiceIdentity> -Parameter <ICloudService>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b35fa-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="b35fa-106">DESCRIPTION</span></span>
<span data-ttu-id="b35fa-107">Criar ou atualizar um serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-107">Create or update a cloud service.</span></span>
<span data-ttu-id="b35fa-108">Observe que algumas propriedades podem ser definidas somente durante a criação de serviços na nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-108">Please note some properties can be set only during cloud service creation.</span></span>

## <span data-ttu-id="b35fa-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b35fa-109">EXAMPLES</span></span>

### <span data-ttu-id="b35fa-110">Exemplo 1: Adicionar extensão RDP ao serviço de nuvem existente</span><span class="sxs-lookup"><span data-stu-id="b35fa-110">Example 1: Add RDP extension to existing cloud service</span></span>
```powershell
# Create RDP extension object
PS C:\> $rdpExtension = New-AzCloudServiceRemoteDesktopExtensionObject -Name "RDPExtension" -Credential $credential -Expiration $expiration -TypeHandlerVersion "1.2.1"
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Add RDP extension to existing cloud service extension object
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension + $rdpExtension
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="b35fa-111">O conjunto de comandos acima adiciona uma extensão RDP ao serviço de nuvem já existente chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b35fa-111">Above set of commands adds a RDP extension to already existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="b35fa-112">Exemplo 2: Remover todas as extensões do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="b35fa-112">Example 2: Remove all extensions from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Set extension to empty list
PS C:\> $cloudService.ExtensionProfile.Extension = @()
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="b35fa-113">O conjunto de comandos acima remove todas as extensões do serviço de nuvem existente chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b35fa-113">Above set of commands removes all extensions from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="b35fa-114">Exemplo 3: Remover extensão RDP do serviço de nuvem</span><span class="sxs-lookup"><span data-stu-id="b35fa-114">Example 3: Remove RDP extension from cloud service</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"
# Remove extension by name RDPExtension
PS C:\> $cloudService.ExtensionProfile.Extension = $cloudService.ExtensionProfile.Extension | Where-Object { $_.Name -ne "RDPExtension" }
# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="b35fa-115">O conjunto de comandos acima remove a extensão RDP do serviço de nuvem existente chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b35fa-115">Above set of commands removes RDP extension from existing cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="b35fa-116">Exemplo 4: Scale-Out /Scale-In de função</span><span class="sxs-lookup"><span data-stu-id="b35fa-116">Example 4: Scale-Out / Scale-In role instances</span></span>
```powershell
# Get existing cloud service
PS C:\> $cloudService = Get-AzCloudService -ResourceGroup "ContosOrg" -CloudServiceName "ContosoCS"

# Scale-out all role instance count by 1
PS C:\> $cloudService.RoleProfile.Role | ForEach-Object {$_.SkuCapacity += 1}

# Scale-in ContosoFrontend role instance count by 1
PS C:\> $role = $cloudService.RoleProfile.Role | Where-Object {$_.Name -eq "ContosoFrontend"}
PS C:\> $role.SkuCapacity -= 1

# Update cloud service configuration as per the new role instance count
PS C:\> $cloudService.Configuration = $configuration

# Update cloud service
PS C:\> $cloudService | Update-AzCloudService
```

<span data-ttu-id="b35fa-117">O conjunto de comandos acima mostra como dimensionar e dimensionar a contagem de instâncias de função para o serviço de nuvem chamado ContosoCS que pertence ao grupo de recursos chamado ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="b35fa-117">Above set of commands shows how to scale-out and scale-in role instance count for cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="b35fa-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b35fa-118">PARAMETERS</span></span>

### <span data-ttu-id="b35fa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b35fa-119">-AsJob</span></span>
<span data-ttu-id="b35fa-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="b35fa-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b35fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b35fa-121">-DefaultProfile</span></span>
<span data-ttu-id="b35fa-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b35fa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b35fa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b35fa-123">-InputObject</span></span>
<span data-ttu-id="b35fa-124">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="b35fa-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b35fa-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b35fa-125">-NoWait</span></span>
<span data-ttu-id="b35fa-126">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="b35fa-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b35fa-127">-Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b35fa-127">-Parameter</span></span>
<span data-ttu-id="b35fa-128">Descreve o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-128">Describes the cloud service.</span></span>
<span data-ttu-id="b35fa-129">Para construir, confira a seção ANOTAÇÕES para as propriedades PARÂMETRO e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="b35fa-129">To construct, see NOTES section for PARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b35fa-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b35fa-130">-Confirm</span></span>
<span data-ttu-id="b35fa-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b35fa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b35fa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b35fa-132">-WhatIf</span></span>
<span data-ttu-id="b35fa-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b35fa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b35fa-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b35fa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b35fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b35fa-135">CommonParameters</span></span>
<span data-ttu-id="b35fa-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b35fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b35fa-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b35fa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b35fa-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="b35fa-138">INPUTS</span></span>

### <span data-ttu-id="b35fa-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="b35fa-139">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

### <span data-ttu-id="b35fa-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b35fa-140">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="b35fa-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="b35fa-141">OUTPUTS</span></span>

### <span data-ttu-id="b35fa-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="b35fa-142">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="b35fa-143">Notas</span><span class="sxs-lookup"><span data-stu-id="b35fa-143">NOTES</span></span>

<span data-ttu-id="b35fa-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="b35fa-144">ALIASES</span></span>

<span data-ttu-id="b35fa-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="b35fa-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b35fa-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="b35fa-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b35fa-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b35fa-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b35fa-148">INPUTOBJECT: <ICloudServiceIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="b35fa-148">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b35fa-149">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b35fa-149">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="b35fa-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="b35fa-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b35fa-151">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b35fa-151">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="b35fa-152">`[RoleInstanceName <String>]`: Nome da instância da função.</span><span class="sxs-lookup"><span data-stu-id="b35fa-152">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="b35fa-153">`[RoleName <String>]`: nome da função.</span><span class="sxs-lookup"><span data-stu-id="b35fa-153">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="b35fa-154">`[SubscriptionId <String>]`: Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b35fa-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b35fa-155">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="b35fa-155">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b35fa-156">`[UpdateDomain <Int32?>]`: especifica um valor inteiro que identifica o domínio de atualização.</span><span class="sxs-lookup"><span data-stu-id="b35fa-156">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="b35fa-157">Os domínios de atualização são identificados com um índice baseado em zero: o primeiro domínio de atualização tem uma ID de 0, o segundo tem uma ID de 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b35fa-157">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

<span data-ttu-id="b35fa-158">PARÂMETRO: <ICloudService> descreve o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-158">PARAMETER <ICloudService>: Describes the cloud service.</span></span>
  - <span data-ttu-id="b35fa-159">`Location <String>`: Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="b35fa-159">`Location <String>`: Resource location.</span></span>
  - <span data-ttu-id="b35fa-160">`[Configuration <String>]`: especifica a configuração do serviço XML (.cscfg) para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-160">`[Configuration <String>]`: Specifies the XML service configuration (.cscfg) for the cloud service.</span></span>
  - <span data-ttu-id="b35fa-161">`[ConfigurationUrl <String>]`: especifica uma URL que se refere ao local da configuração do serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="b35fa-161">`[ConfigurationUrl <String>]`: Specifies a URL that refers to the location of the service configuration in the Blob service.</span></span> <span data-ttu-id="b35fa-162">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b35fa-162">The service package URL  can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="b35fa-163">Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="b35fa-163">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="b35fa-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: descreve um perfil de extensão de serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-164">`[ExtensionProfile <ICloudServiceExtensionProfile>]`: Describes a cloud service extension profile.</span></span>
    - <span data-ttu-id="b35fa-165">`[Extension <IExtension[]>]`: Lista de extensões do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-165">`[Extension <IExtension[]>]`: List of extensions for the cloud service.</span></span>
      - <span data-ttu-id="b35fa-166">`[AutoUpgradeMinorVersion <Boolean?>]`: especifique explicitamente se a plataforma pode atualizar automaticamente o tipoHandlerVersion para versões secundárias mais altas quando elas se tornam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b35fa-166">`[AutoUpgradeMinorVersion <Boolean?>]`: Explicitly specify whether platform can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>
      - <span data-ttu-id="b35fa-167">`[ForceUpdateTag <String>]`: Marque para forçar a aplicação das configurações públicas e protegidas fornecidas.</span><span class="sxs-lookup"><span data-stu-id="b35fa-167">`[ForceUpdateTag <String>]`: Tag to force apply the provided public and protected settings.</span></span>         <span data-ttu-id="b35fa-168">Alterar o valor da marca permite executar a extensão de forma a executar a extensão sem alterar as configurações públicas ou protegidas.</span><span class="sxs-lookup"><span data-stu-id="b35fa-168">Changing the tag value allows for re-running the extension without changing any of the public or protected settings.</span></span>         <span data-ttu-id="b35fa-169">Se forceUpdateTag não for alterado, as atualizações para configurações públicas ou protegidas ainda serão aplicadas pelo manipulador.</span><span class="sxs-lookup"><span data-stu-id="b35fa-169">If forceUpdateTag is not changed, updates to public or protected settings would still be applied by the handler.</span></span>         <span data-ttu-id="b35fa-170">Se nem forçarUpdateTag nem nenhuma das configurações públicas ou protegidas mudar, a extensão fluiria para a instância de função com o mesmo número de sequência, e a implementação de manipuladores decidirá se a executará ou não.</span><span class="sxs-lookup"><span data-stu-id="b35fa-170">If neither forceUpdateTag nor any of public or protected settings change, extension would flow to the role instance with the same sequence-number, and         it is up to handler implementation whether to re-run it or not</span></span>
      - <span data-ttu-id="b35fa-171">`[Name <String>]`: o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-171">`[Name <String>]`: The name of the extension.</span></span>
      - <span data-ttu-id="b35fa-172">`[ProtectedSetting <String>]`: Configurações protegidas para a extensão que são criptografadas antes de enviar para a instância de função.</span><span class="sxs-lookup"><span data-stu-id="b35fa-172">`[ProtectedSetting <String>]`: Protected settings for the extension which are encrypted before sent to the role instance.</span></span>
      - <span data-ttu-id="b35fa-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b35fa-173">`[ProtectedSettingFromKeyVaultSecretUrl <String>]`:</span></span> 
      - <span data-ttu-id="b35fa-174">`[Publisher <String>]`: o nome do editor do manipulador de extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-174">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
      - <span data-ttu-id="b35fa-175">`[RolesAppliedTo <String[]>]`: Lista opcional de funções para aplicar essa extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-175">`[RolesAppliedTo <String[]>]`: Optional list of roles to apply this extension.</span></span> <span data-ttu-id="b35fa-176">Se a propriedade não for especificada ou '\*' for especificada, a extensão será aplicada a todas as funções no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-176">If property is not specified or '\*' is specified, extension is applied to all roles in the cloud service.</span></span>
      - <span data-ttu-id="b35fa-177">`[Setting <String>]`: Configurações públicas para a extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-177">`[Setting <String>]`: Public settings for the extension.</span></span> <span data-ttu-id="b35fa-178">Para extensões JSON, essas são as configurações JSON para a extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-178">For JSON extensions, this is the JSON settings for the extension.</span></span> <span data-ttu-id="b35fa-179">Para Extensão XML (como RDP), essa é a configuração XML para a extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-179">For XML Extension (like RDP), this is the XML setting for the extension.</span></span>
      - <span data-ttu-id="b35fa-180">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="b35fa-180">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="b35fa-181">`[Type <String>]`: especifica o tipo da extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-181">`[Type <String>]`: Specifies the type of the extension.</span></span>
      - <span data-ttu-id="b35fa-182">`[TypeHandlerVersion <String>]`: especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-182">`[TypeHandlerVersion <String>]`: Specifies the version of the extension.</span></span> <span data-ttu-id="b35fa-183">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="b35fa-183">Specifies the version of the extension.</span></span> <span data-ttu-id="b35fa-184">Se esse elemento não for especificado ou um asterisco (\*) for usado como o valor, a versão mais recente da extensão será usada.</span><span class="sxs-lookup"><span data-stu-id="b35fa-184">If this element is not specified or an asterisk (\*) is used as the value, the latest version of the extension is used.</span></span> <span data-ttu-id="b35fa-185">Se o valor for especificado com um número de versão principal e um asterisco como o número da versão secundária (X.), a versão secundária mais recente da versão principal especificada será selecionada.</span><span class="sxs-lookup"><span data-stu-id="b35fa-185">If the value is specified with a major version number and an asterisk as the minor version number (X.), the latest minor version of the specified major version is selected.</span></span> <span data-ttu-id="b35fa-186">Se um número de versão principal e um número de versão secundária forem especificados (X.Y), a versão de extensão específica será selecionada.</span><span class="sxs-lookup"><span data-stu-id="b35fa-186">If a major version number and a minor version number are specified (X.Y), the specific extension version is selected.</span></span> <span data-ttu-id="b35fa-187">Se uma versão for especificada, uma atualização automática será executada na instância da função.</span><span class="sxs-lookup"><span data-stu-id="b35fa-187">If a version is specified, an auto-upgrade is performed on the role instance.</span></span>
  - <span data-ttu-id="b35fa-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Perfil de Rede do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-188">`[NetworkProfile <ICloudServiceNetworkProfile>]`: Network Profile for the cloud service.</span></span>
    - <span data-ttu-id="b35fa-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: a lista de configurações de balanceador de carga para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-189">`[LoadBalancerConfiguration <ILoadBalancerConfiguration[]>]`: The list of load balancer configurations for the cloud service.</span></span>
      - <span data-ttu-id="b35fa-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: Lista de IP</span><span class="sxs-lookup"><span data-stu-id="b35fa-190">`[FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>]`: List of IP</span></span>
        - <span data-ttu-id="b35fa-191">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="b35fa-191">`[Name <String>]`:</span></span> 
        - <span data-ttu-id="b35fa-192">`[PrivateIPAddress <String>]`: O endereço IP particular referenciado pelo serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-192">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
        - <span data-ttu-id="b35fa-193">`[PublicIPAddressId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="b35fa-193">`[PublicIPAddressId <String>]`: Resource Id</span></span>
        - <span data-ttu-id="b35fa-194">`[SubnetId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="b35fa-194">`[SubnetId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="b35fa-195">`[Name <String>]`: Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="b35fa-195">`[Name <String>]`: Resource Name</span></span>
    - <span data-ttu-id="b35fa-196">`[SwappableCloudService <ISubResource>]`:</span><span class="sxs-lookup"><span data-stu-id="b35fa-196">`[SwappableCloudService <ISubResource>]`:</span></span> 
      - <span data-ttu-id="b35fa-197">`[Id <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="b35fa-197">`[Id <String>]`: Resource Id</span></span>
  - <span data-ttu-id="b35fa-198">`[OSProfile <ICloudServiceOSProfile>]`: descreve o perfil do sistema operacional para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-198">`[OSProfile <ICloudServiceOSProfile>]`: Describes the OS profile for the cloud service.</span></span>
    - <span data-ttu-id="b35fa-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: especifica o conjunto de certificados que devem ser instalados nas instâncias de função.</span><span class="sxs-lookup"><span data-stu-id="b35fa-199">`[Secret <ICloudServiceVaultSecretGroup[]>]`: Specifies set of certificates that should be installed onto the role instances.</span></span>
      - <span data-ttu-id="b35fa-200">`[SourceVaultId <String>]`: ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="b35fa-200">`[SourceVaultId <String>]`: Resource Id</span></span>
      - <span data-ttu-id="b35fa-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: a lista de referências chave do cofre no SourceVault que contêm certificados.</span><span class="sxs-lookup"><span data-stu-id="b35fa-201">`[VaultCertificate <ICloudServiceVaultCertificate[]>]`: The list of key vault references in SourceVault which contain certificates.</span></span>
        - <span data-ttu-id="b35fa-202">`[CertificateUrl <String>]`: Esta é a URL de um certificado que foi carregado para o Cofre de Chaves como um segredo.</span><span class="sxs-lookup"><span data-stu-id="b35fa-202">`[CertificateUrl <String>]`: This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
  - <span data-ttu-id="b35fa-203">`[PackageUrl <String>]`: especifica uma URL que se refere ao local do pacote de serviço no serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="b35fa-203">`[PackageUrl <String>]`: Specifies a URL that refers to the location of the service package in the Blob service.</span></span> <span data-ttu-id="b35fa-204">A URL do pacote de serviço pode ser URI de assinatura de acesso compartilhado (SAS) de qualquer conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b35fa-204">The service package URL can be Shared Access Signature (SAS) URI from any storage account.</span></span>         <span data-ttu-id="b35fa-205">Essa é uma propriedade somente gravação e não é retornada em chamadas GET.</span><span class="sxs-lookup"><span data-stu-id="b35fa-205">This is a write-only property and is not returned in GET calls.</span></span>
  - <span data-ttu-id="b35fa-206">`[RoleProfile <ICloudServiceRoleProfile>]`: descreve o perfil de função do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-206">`[RoleProfile <ICloudServiceRoleProfile>]`: Describes the role profile for the cloud service.</span></span>
    - <span data-ttu-id="b35fa-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: Lista de funções do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-207">`[Role <ICloudServiceRoleProfileProperties[]>]`: List of roles for the cloud service.</span></span>
      - <span data-ttu-id="b35fa-208">`[Name <String>]`: Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b35fa-208">`[Name <String>]`: Resource name.</span></span>
      - <span data-ttu-id="b35fa-209">`[SkuCapacity <Int64?>]`: especifica o número de instâncias de função no serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-209">`[SkuCapacity <Int64?>]`: Specifies the number of role instances in the cloud service.</span></span>
      - <span data-ttu-id="b35fa-210">`[SkuName <String>]`: o nome da sKU.</span><span class="sxs-lookup"><span data-stu-id="b35fa-210">`[SkuName <String>]`: The sku name.</span></span> <span data-ttu-id="b35fa-211">OBSERVAÇÃO: se a nova SKU não for suportada no hardware em que o serviço de nuvem está atualmente, você precisará excluir e recriar o serviço de nuvem ou voltar para a SKU antiga.</span><span class="sxs-lookup"><span data-stu-id="b35fa-211">NOTE: If the new SKU is not supported on the hardware the cloud service is currently on, you need to delete and recreate the cloud service or move back to the old sku.</span></span>
      - <span data-ttu-id="b35fa-212">`[SkuTier <String>]`: especifica o nível do serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-212">`[SkuTier <String>]`: Specifies the tier of the cloud service.</span></span> <span data-ttu-id="b35fa-213">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="b35fa-213">Possible Values are</span></span> <br /><br /> <span data-ttu-id="b35fa-214">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="b35fa-214">**Standard**</span></span> <br /><br /> <span data-ttu-id="b35fa-215">**Basic**</span><span class="sxs-lookup"><span data-stu-id="b35fa-215">**Basic**</span></span>
  - <span data-ttu-id="b35fa-216">`[StartCloudService <Boolean?>]`: (Opcional) Indica se o serviço de nuvem deve ser iniciar imediatamente após sua criação.</span><span class="sxs-lookup"><span data-stu-id="b35fa-216">`[StartCloudService <Boolean?>]`: (Optional) Indicates whether to start the cloud service immediately after it is created.</span></span> <span data-ttu-id="b35fa-217">O valor padrão é `true` .</span><span class="sxs-lookup"><span data-stu-id="b35fa-217">The default value is `true`.</span></span>         <span data-ttu-id="b35fa-218">Se for falso, o modelo de serviço ainda será implantado, mas o código não será executado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="b35fa-218">If false, the service model is still deployed, but the code is not run immediately.</span></span> <span data-ttu-id="b35fa-219">Em vez disso, o serviço é PoweredOff até que você ligue para Iniciar, momento em que o serviço será iniciado.</span><span class="sxs-lookup"><span data-stu-id="b35fa-219">Instead, the service is PoweredOff until you call Start, at which time the service will be started.</span></span> <span data-ttu-id="b35fa-220">Um serviço implantado ainda incorre em encargos, mesmo que ele esteja desligado.</span><span class="sxs-lookup"><span data-stu-id="b35fa-220">A deployed service still incurs charges, even if it is poweredoff.</span></span>
  - <span data-ttu-id="b35fa-221">`[Tag <ICloudServiceTags>]`: Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b35fa-221">`[Tag <ICloudServiceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="b35fa-222">`[(Any) <String>]`: indica que qualquer propriedade pode ser adicionada a este objeto.</span><span class="sxs-lookup"><span data-stu-id="b35fa-222">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="b35fa-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Modo de atualização para o serviço de nuvem.</span><span class="sxs-lookup"><span data-stu-id="b35fa-223">`[UpgradeMode <CloudServiceUpgradeMode?>]`: Update mode for the cloud service.</span></span> <span data-ttu-id="b35fa-224">As instâncias de função são alocadas para atualizar domínios quando o serviço é implantado.</span><span class="sxs-lookup"><span data-stu-id="b35fa-224">Role instances are allocated to update domains when the service is deployed.</span></span> <span data-ttu-id="b35fa-225">As atualizações podem ser iniciadas manualmente em cada domínio de atualização ou iniciadas automaticamente em todos os domínios de atualização.</span><span class="sxs-lookup"><span data-stu-id="b35fa-225">Updates can be initiated manually in each update domain or initiated automatically in all update domains.</span></span>         <span data-ttu-id="b35fa-226">Os valores possíveis são</span><span class="sxs-lookup"><span data-stu-id="b35fa-226">Possible Values are</span></span> <br /><br /><span data-ttu-id="b35fa-227">**Automático**</span><span class="sxs-lookup"><span data-stu-id="b35fa-227">**Auto**</span></span><br /><br /><span data-ttu-id="b35fa-228">**Manual**</span><span class="sxs-lookup"><span data-stu-id="b35fa-228">**Manual**</span></span> <br /><br /><span data-ttu-id="b35fa-229">**Simultânea**</span><span class="sxs-lookup"><span data-stu-id="b35fa-229">**Simultaneous**</span></span><br /><br />         <span data-ttu-id="b35fa-230">Se não especificado, o valor padrão será Automático. Se definido como Manual, PUT UpdateDomain deverá ser chamado para aplicar a atualização.</span><span class="sxs-lookup"><span data-stu-id="b35fa-230">If not specified, the default value is Auto. If set to Manual, PUT UpdateDomain must be called to apply the update.</span></span> <span data-ttu-id="b35fa-231">Se definido como Automático, a atualização será aplicada automaticamente a cada domínio de atualização em sequência.</span><span class="sxs-lookup"><span data-stu-id="b35fa-231">If set to Auto, the update is automatically applied to each update domain in sequence.</span></span>

## <span data-ttu-id="b35fa-232">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b35fa-232">RELATED LINKS</span></span>

