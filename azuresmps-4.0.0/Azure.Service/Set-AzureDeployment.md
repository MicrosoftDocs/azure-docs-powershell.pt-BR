---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7F51F534-6C64-4983-A08F-4732A39C2E7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 52c62f3d29b4cd2c87fd5606ca013eb03958fb62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946064"
---
# <span data-ttu-id="219bc-101">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="219bc-101">Set-AzureDeployment</span></span>

## <span data-ttu-id="219bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="219bc-102">SYNOPSIS</span></span>
<span data-ttu-id="219bc-103">Modifica o status, as definições de configuração ou o modo de atualização de uma implantação.</span><span class="sxs-lookup"><span data-stu-id="219bc-103">Modifies the status, configuration settings, or upgrade mode of a deployment.</span></span>

## <span data-ttu-id="219bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="219bc-104">SYNTAX</span></span>

### <span data-ttu-id="219bc-105">Atualização</span><span class="sxs-lookup"><span data-stu-id="219bc-105">Upgrade</span></span>
```
Set-AzureDeployment [-Upgrade] [-ServiceName] <String> [-Package] <String> [-Configuration] <String>
 [-Slot] <String> [[-Mode] <String>] [[-Label] <String>] [[-RoleName] <String>] [-Force]
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="219bc-106">Configurar</span><span class="sxs-lookup"><span data-stu-id="219bc-106">Config</span></span>
```
Set-AzureDeployment [-Config] [-ServiceName] <String> [-Configuration] <String> [-Slot] <String>
 [[-ExtensionConfiguration] <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="219bc-107">Situação</span><span class="sxs-lookup"><span data-stu-id="219bc-107">Status</span></span>
```
Set-AzureDeployment [-Status] [-ServiceName] <String> [-Slot] <String> [-NewStatus] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="219bc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="219bc-108">DESCRIPTION</span></span>
<span data-ttu-id="219bc-109">O cmdlet **set-AzureDeployment** modifica o status, as definições de configuração ou o modo de atualização de uma implantação do Azure.</span><span class="sxs-lookup"><span data-stu-id="219bc-109">The **Set-AzureDeployment** cmdlet modifies the status, configuration settings, or upgrade mode of an Azure deployment.</span></span>
<span data-ttu-id="219bc-110">Você pode alterar o status da implantação para a execução ou a suspensão.</span><span class="sxs-lookup"><span data-stu-id="219bc-110">You can change the status of the deployment to either Running or Suspended.</span></span>
<span data-ttu-id="219bc-111">Você pode alterar o arquivo. cscfg para a implantação.</span><span class="sxs-lookup"><span data-stu-id="219bc-111">You can change the .cscfg file for the deployment.</span></span>
<span data-ttu-id="219bc-112">Você pode definir o modo de atualização e atualizar arquivos de configuração.</span><span class="sxs-lookup"><span data-stu-id="219bc-112">You can set the upgrade mode and update configuration files.</span></span>
<span data-ttu-id="219bc-113">Use o cmdlet **set-AzureWalkUpgradeDomain** para iniciar uma atualização.</span><span class="sxs-lookup"><span data-stu-id="219bc-113">Use the **Set-AzureWalkUpgradeDomain** cmdlet to initiate an upgrade.</span></span>

## <span data-ttu-id="219bc-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="219bc-114">EXAMPLES</span></span>

### <span data-ttu-id="219bc-115">Exemplo 1: alterar o status de uma implantação</span><span class="sxs-lookup"><span data-stu-id="219bc-115">Example 1: Change the status of a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Status -ServiceName "ContosoService" -Slot "Production" -NewStatus "Running"
```

<span data-ttu-id="219bc-116">Esse comando define o status da implantação do serviço chamado ContosoService no ambiente de produção a ser executado.</span><span class="sxs-lookup"><span data-stu-id="219bc-116">This command sets the status of the deployment for the service named ContosoService in the production environment to Running.</span></span>

### <span data-ttu-id="219bc-117">Exemplo 2: atribuir um arquivo de configuração diferente a uma implantação</span><span class="sxs-lookup"><span data-stu-id="219bc-117">Example 2: Assign a different configuration file to a deployment</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Slot "Staging" -Configuration "C:\Temp\MyServiceConfig.Cloud.csfg"
```

<span data-ttu-id="219bc-118">Esse comando atribui um arquivo de configuração diferente para a implantação do serviço chamado ContosoService no ambiente de preparo.</span><span class="sxs-lookup"><span data-stu-id="219bc-118">This command assigns a different configuration file for the deployment for the service named ContosoService in the staging environment.</span></span>

### <span data-ttu-id="219bc-119">Exemplo 3: definir o modo de atualização para automático</span><span class="sxs-lookup"><span data-stu-id="219bc-119">Example 3: Set the upgrade mode to Auto</span></span>
```
PS C:\> Set-AzureDeployment -Upgrade -ServiceName "ContosoService" -Mode Auto -Package "C:\packages\ContosoApp.cspkg" -Configuration "C:\Config\ContosoServiceConfig.Cloud.csfg"
```

<span data-ttu-id="219bc-120">Esse comando define o modo de atualização como automático e especifica um pacote de atualização e um novo arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="219bc-120">This command sets the upgrade mode to Auto, and specifies an upgrade package and a new configuration file.</span></span>

### <span data-ttu-id="219bc-121">Exemplo 4: instalar a configuração da extensão em um serviço</span><span class="sxs-lookup"><span data-stu-id="219bc-121">Example 4: Install extension configuration in a service</span></span>
```
PS C:\> Set-AzureDeployment -Config -ServiceName "ContosoService" -Mode "Automatic" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Slot "Production" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="219bc-122">Esse comando instala a configuração de extensão no serviço de nuvem especificado e as aplica em funções.</span><span class="sxs-lookup"><span data-stu-id="219bc-122">This command installs the extension configuration in the specified Cloud Service and applies them on roles.</span></span>

## <span data-ttu-id="219bc-123">OS</span><span class="sxs-lookup"><span data-stu-id="219bc-123">PARAMETERS</span></span>

### <span data-ttu-id="219bc-124">-Config</span><span class="sxs-lookup"><span data-stu-id="219bc-124">-Config</span></span>
<span data-ttu-id="219bc-125">Especifica que esse cmdlet modifica a configuração da implantação.</span><span class="sxs-lookup"><span data-stu-id="219bc-125">Specifies that this cmdlet modifies the configuration of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Config
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-126">-Configuração</span><span class="sxs-lookup"><span data-stu-id="219bc-126">-Configuration</span></span>
<span data-ttu-id="219bc-127">Especifica o caminho completo de um arquivo de configuração. cscfg.</span><span class="sxs-lookup"><span data-stu-id="219bc-127">Specifies the full path of a .cscfg configuration file.</span></span>
<span data-ttu-id="219bc-128">Você pode especificar um arquivo de configuração para uma atualização ou alteração de configuração.</span><span class="sxs-lookup"><span data-stu-id="219bc-128">You can specify a configuration file for an upgrade or configuration change.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade, Config
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-129">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="219bc-129">-ExtensionConfiguration</span></span>
<span data-ttu-id="219bc-130">Especifica uma matriz de objetos de configuração de extensão.</span><span class="sxs-lookup"><span data-stu-id="219bc-130">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: Upgrade, Config
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-131">-Force</span><span class="sxs-lookup"><span data-stu-id="219bc-131">-Force</span></span>
<span data-ttu-id="219bc-132">Indica que o cmdlet executa uma atualização forçada.</span><span class="sxs-lookup"><span data-stu-id="219bc-132">Indicates that cmdlet performs a forced upgrade.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-133">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="219bc-133">-InformationAction</span></span>
<span data-ttu-id="219bc-134">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="219bc-134">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="219bc-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="219bc-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="219bc-136">Contínuo</span><span class="sxs-lookup"><span data-stu-id="219bc-136">Continue</span></span>
- <span data-ttu-id="219bc-137">Ignorar</span><span class="sxs-lookup"><span data-stu-id="219bc-137">Ignore</span></span>
- <span data-ttu-id="219bc-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="219bc-138">Inquire</span></span>
- <span data-ttu-id="219bc-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="219bc-139">SilentlyContinue</span></span>
- <span data-ttu-id="219bc-140">Finaliza</span><span class="sxs-lookup"><span data-stu-id="219bc-140">Stop</span></span>
- <span data-ttu-id="219bc-141">Suspensão</span><span class="sxs-lookup"><span data-stu-id="219bc-141">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="219bc-142">-InformationVariable</span></span>
<span data-ttu-id="219bc-143">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="219bc-143">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-144">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="219bc-144">-Label</span></span>
<span data-ttu-id="219bc-145">Especifica um rótulo para a implantação atualizada.</span><span class="sxs-lookup"><span data-stu-id="219bc-145">Specifies a label for the upgraded deployment.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-146">-Mode</span><span class="sxs-lookup"><span data-stu-id="219bc-146">-Mode</span></span>
<span data-ttu-id="219bc-147">Especifica o modo de atualização.</span><span class="sxs-lookup"><span data-stu-id="219bc-147">Specifies the mode of upgrade.</span></span>
<span data-ttu-id="219bc-148">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="219bc-148">Valid values are:</span></span> 

- <span data-ttu-id="219bc-149">Automático</span><span class="sxs-lookup"><span data-stu-id="219bc-149">Auto</span></span> 
- <span data-ttu-id="219bc-150">Manual</span><span class="sxs-lookup"><span data-stu-id="219bc-150">Manual</span></span> 
- <span data-ttu-id="219bc-151">Simultânea</span><span class="sxs-lookup"><span data-stu-id="219bc-151">Simultaneous</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-152">-NewStatus</span><span class="sxs-lookup"><span data-stu-id="219bc-152">-NewStatus</span></span>
<span data-ttu-id="219bc-153">Especifica o status de destino para a implantação.</span><span class="sxs-lookup"><span data-stu-id="219bc-153">Specifies the target status for the deployment.</span></span>
<span data-ttu-id="219bc-154">Os valores válidos são: running e Suspended.</span><span class="sxs-lookup"><span data-stu-id="219bc-154">Valid values are: Running and Suspended.</span></span>

```yaml
Type: String
Parameter Sets: Status
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-155">-Package</span><span class="sxs-lookup"><span data-stu-id="219bc-155">-Package</span></span>
<span data-ttu-id="219bc-156">Especifica o caminho completo de um arquivo de pacote de atualização.</span><span class="sxs-lookup"><span data-stu-id="219bc-156">Specifies the full path of an upgrade package file.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-157">-Perfil</span><span class="sxs-lookup"><span data-stu-id="219bc-157">-Profile</span></span>
<span data-ttu-id="219bc-158">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="219bc-158">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="219bc-159">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="219bc-159">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-160">-RoleName</span><span class="sxs-lookup"><span data-stu-id="219bc-160">-RoleName</span></span>
<span data-ttu-id="219bc-161">Especifica o nome da função a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="219bc-161">Specifies the name of the role to upgrade.</span></span>

```yaml
Type: String
Parameter Sets: Upgrade
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-162">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="219bc-162">-ServiceName</span></span>
<span data-ttu-id="219bc-163">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="219bc-163">Specifies the name of the Azure service of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-164">-Slot</span><span class="sxs-lookup"><span data-stu-id="219bc-164">-Slot</span></span>
<span data-ttu-id="219bc-165">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="219bc-165">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="219bc-166">Os valores válidos são: produção e preparação.</span><span class="sxs-lookup"><span data-stu-id="219bc-166">Valid values are: Production and Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-167">-Status</span><span class="sxs-lookup"><span data-stu-id="219bc-167">-Status</span></span>
<span data-ttu-id="219bc-168">Especifica que esse cmdlet altera o status da implantação.</span><span class="sxs-lookup"><span data-stu-id="219bc-168">Specifies that this cmdlet changes the status of the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Status
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-169">-Atualização</span><span class="sxs-lookup"><span data-stu-id="219bc-169">-Upgrade</span></span>
<span data-ttu-id="219bc-170">Especifica que esse cmdlet atualize a implantação.</span><span class="sxs-lookup"><span data-stu-id="219bc-170">Specifies that this cmdlet upgrades the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Upgrade
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219bc-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219bc-171">CommonParameters</span></span>
<span data-ttu-id="219bc-172">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219bc-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219bc-173">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219bc-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219bc-174">SENSORES</span><span class="sxs-lookup"><span data-stu-id="219bc-174">INPUTS</span></span>

## <span data-ttu-id="219bc-175">EXIBE</span><span class="sxs-lookup"><span data-stu-id="219bc-175">OUTPUTS</span></span>

## <span data-ttu-id="219bc-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="219bc-176">NOTES</span></span>

## <span data-ttu-id="219bc-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="219bc-177">RELATED LINKS</span></span>

[<span data-ttu-id="219bc-178">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="219bc-178">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="219bc-179">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="219bc-179">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="219bc-180">Mover-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="219bc-180">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="219bc-181">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="219bc-181">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="219bc-182">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="219bc-182">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="219bc-183">Set-AzureWalkUpgradeDomain</span><span class="sxs-lookup"><span data-stu-id="219bc-183">Set-AzureWalkUpgradeDomain</span></span>](./Set-AzureWalkUpgradeDomain.md)


