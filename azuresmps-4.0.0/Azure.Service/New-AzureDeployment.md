---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945929"
---
# <span data-ttu-id="387d1-101">New-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="387d1-101">New-AzureDeployment</span></span>

## <span data-ttu-id="387d1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="387d1-102">SYNOPSIS</span></span>
<span data-ttu-id="387d1-103">Cria uma implantação a partir de um serviço.</span><span class="sxs-lookup"><span data-stu-id="387d1-103">Creates a deployment from a service.</span></span>

## <span data-ttu-id="387d1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="387d1-104">SYNTAX</span></span>

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="387d1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="387d1-105">DESCRIPTION</span></span>
<span data-ttu-id="387d1-106">O cmdlet **New-AzureDeployment** cria uma implantação do Azure a partir de um serviço que inclui funções da Web e funções de trabalho.</span><span class="sxs-lookup"><span data-stu-id="387d1-106">The **New-AzureDeployment** cmdlet creates an Azure deployment from a service that comprises web roles and worker roles.</span></span>
<span data-ttu-id="387d1-107">Esse cmdlet cria uma implantação com base em um arquivo de pacote (. cspkg) e um arquivo de configuração de serviço (. cscfg).</span><span class="sxs-lookup"><span data-stu-id="387d1-107">This cmdlet creates a deployment based on a package file (.cspkg) and a service configuration file (.cscfg).</span></span>
<span data-ttu-id="387d1-108">Especifique um nome exclusivo no ambiente de implantação.</span><span class="sxs-lookup"><span data-stu-id="387d1-108">Specify a name that is unique within deployment environment.</span></span>

<span data-ttu-id="387d1-109">Use o cmdlet **New-AzureVM** para criar uma implantação com base nas máquinas virtuais do Azure.</span><span class="sxs-lookup"><span data-stu-id="387d1-109">Use the **New-AzureVM** cmdlet to create a deployment based on Azure virtual machines.</span></span>

## <span data-ttu-id="387d1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="387d1-110">EXAMPLES</span></span>

### <span data-ttu-id="387d1-111">Exemplo 1: criar uma implantação</span><span class="sxs-lookup"><span data-stu-id="387d1-111">Example 1: Create a deployment</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

<span data-ttu-id="387d1-112">Esse comando cria uma implantação de produção com base em um pacote chamado ContosoPackage. cspkg e uma configuração chamada ContosoConfiguration. cscfg.</span><span class="sxs-lookup"><span data-stu-id="387d1-112">This command creates a production deployment based on a package named ContosoPackage.cspkg and a configuration named ContosoConfiguration.cscfg.</span></span>
<span data-ttu-id="387d1-113">O comando especifica um rótulo para a implantação.</span><span class="sxs-lookup"><span data-stu-id="387d1-113">The command specifies a label for the deployment.</span></span>
<span data-ttu-id="387d1-114">Ele não especifica um nome.</span><span class="sxs-lookup"><span data-stu-id="387d1-114">It does not specify a name.</span></span>
<span data-ttu-id="387d1-115">Esse cmdlet cria um GUID como o nome.</span><span class="sxs-lookup"><span data-stu-id="387d1-115">This cmdlet creates a GUID as the name.</span></span>

### <span data-ttu-id="387d1-116">Exemplo 2: criar uma implantação com base em uma configuração de extensão</span><span class="sxs-lookup"><span data-stu-id="387d1-116">Example 2: Create a deployment based on an extension configuration</span></span>
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

<span data-ttu-id="387d1-117">Esse comando cria uma implantação de produção com base em um pacote e uma configuração.</span><span class="sxs-lookup"><span data-stu-id="387d1-117">This command creates a production deployment based on a package and configuration.</span></span>
<span data-ttu-id="387d1-118">O comando especifica uma configuração de extensão chamada ContosoExtensionConfig. cscfg.</span><span class="sxs-lookup"><span data-stu-id="387d1-118">The command specifies an extension configuration named ContosoExtensionConfig.cscfg.</span></span>
<span data-ttu-id="387d1-119">Esse cmdlet cria GUIDs como o nome e o rótulo.</span><span class="sxs-lookup"><span data-stu-id="387d1-119">This cmdlet creates GUIDs as the name and the label.</span></span>

## <span data-ttu-id="387d1-120">OS</span><span class="sxs-lookup"><span data-stu-id="387d1-120">PARAMETERS</span></span>

### <span data-ttu-id="387d1-121">-Configuração</span><span class="sxs-lookup"><span data-stu-id="387d1-121">-Configuration</span></span>
<span data-ttu-id="387d1-122">Especifica o caminho completo de um arquivo de configuração de serviço.</span><span class="sxs-lookup"><span data-stu-id="387d1-122">Specifies the full path of a service configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-123">-DoNotStart</span><span class="sxs-lookup"><span data-stu-id="387d1-123">-DoNotStart</span></span>
<span data-ttu-id="387d1-124">Especifica que esse cmdlet não inicia a implantação.</span><span class="sxs-lookup"><span data-stu-id="387d1-124">Specifies that this cmdlet does not start the deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-125">-ExtensionConfiguration</span><span class="sxs-lookup"><span data-stu-id="387d1-125">-ExtensionConfiguration</span></span>
<span data-ttu-id="387d1-126">Especifica uma matriz de objetos de configuração de extensão.</span><span class="sxs-lookup"><span data-stu-id="387d1-126">Specifies an array of extension configuration objects.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="387d1-127">-InformationAction</span></span>
<span data-ttu-id="387d1-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="387d1-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="387d1-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="387d1-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="387d1-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="387d1-130">Continue</span></span>
- <span data-ttu-id="387d1-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="387d1-131">Ignore</span></span>
- <span data-ttu-id="387d1-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="387d1-132">Inquire</span></span>
- <span data-ttu-id="387d1-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="387d1-133">SilentlyContinue</span></span>
- <span data-ttu-id="387d1-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="387d1-134">Stop</span></span>
- <span data-ttu-id="387d1-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="387d1-135">Suspend</span></span>

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

### <span data-ttu-id="387d1-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="387d1-136">-InformationVariable</span></span>
<span data-ttu-id="387d1-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="387d1-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="387d1-138">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="387d1-138">-Label</span></span>
<span data-ttu-id="387d1-139">Especifica um nome de rótulo para a implantação.</span><span class="sxs-lookup"><span data-stu-id="387d1-139">Specifies a label name for the deployment.</span></span>
<span data-ttu-id="387d1-140">Se você não especificar um rótulo, esse cmdlet usará um GUID.</span><span class="sxs-lookup"><span data-stu-id="387d1-140">If you do not specify a label, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="387d1-141">-Name</span></span>
<span data-ttu-id="387d1-142">Especifica um nome de implantação.</span><span class="sxs-lookup"><span data-stu-id="387d1-142">Specifies a deployment name.</span></span>
<span data-ttu-id="387d1-143">Se você não especificar um nome, esse cmdlet usará um GUID.</span><span class="sxs-lookup"><span data-stu-id="387d1-143">If you do not specify a name, this cmdlet uses a GUID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-144">-Package</span><span class="sxs-lookup"><span data-stu-id="387d1-144">-Package</span></span>
<span data-ttu-id="387d1-145">Especifica o caminho ou o URI de um arquivo. cspkg no armazenamento na mesma assinatura ou projeto.</span><span class="sxs-lookup"><span data-stu-id="387d1-145">Specifies the path or URI of a .cspkg file in storage within the same subscription or project.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-146">-Perfil</span><span class="sxs-lookup"><span data-stu-id="387d1-146">-Profile</span></span>
<span data-ttu-id="387d1-147">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="387d1-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="387d1-148">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="387d1-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="387d1-149">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="387d1-149">-ServiceName</span></span>
<span data-ttu-id="387d1-150">Especifica o nome do serviço do Azure para a implantação.</span><span class="sxs-lookup"><span data-stu-id="387d1-150">Specifies the name of the Azure service for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-151">-Slot</span><span class="sxs-lookup"><span data-stu-id="387d1-151">-Slot</span></span>
<span data-ttu-id="387d1-152">Especifica o ambiente em que esse cmdlet cria a implantação.</span><span class="sxs-lookup"><span data-stu-id="387d1-152">Specifies the environment where this cmdlet creates the deployment.</span></span>
<span data-ttu-id="387d1-153">Os valores válidos são: preparação e produção.</span><span class="sxs-lookup"><span data-stu-id="387d1-153">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="387d1-154">O valor padrão é produção.</span><span class="sxs-lookup"><span data-stu-id="387d1-154">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-155">-TreatWarningsAsError</span><span class="sxs-lookup"><span data-stu-id="387d1-155">-TreatWarningsAsError</span></span>
<span data-ttu-id="387d1-156">Especifica que as mensagens de aviso são erros.</span><span class="sxs-lookup"><span data-stu-id="387d1-156">Specifies that warning messages are errors.</span></span>
<span data-ttu-id="387d1-157">Se você especificar esse parâmetro, uma mensagem de aviso causará falha na implantação.</span><span class="sxs-lookup"><span data-stu-id="387d1-157">If you specify this parameter, a warning message causes the deployment to fail.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="387d1-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387d1-158">CommonParameters</span></span>
<span data-ttu-id="387d1-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="387d1-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387d1-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387d1-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387d1-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="387d1-161">INPUTS</span></span>

## <span data-ttu-id="387d1-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="387d1-162">OUTPUTS</span></span>

## <span data-ttu-id="387d1-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="387d1-163">NOTES</span></span>

## <span data-ttu-id="387d1-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="387d1-164">RELATED LINKS</span></span>

[<span data-ttu-id="387d1-165">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="387d1-165">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="387d1-166">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="387d1-166">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="387d1-167">Mover-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="387d1-167">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="387d1-168">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="387d1-168">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="387d1-169">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="387d1-169">Remove-AzureDeployment</span></span>](./Remove-AzureDeployment.md)

[<span data-ttu-id="387d1-170">Set-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="387d1-170">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


