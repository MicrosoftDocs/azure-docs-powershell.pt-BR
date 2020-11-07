---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945883"
---
# <span data-ttu-id="ae5ac-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ae5ac-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="ae5ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5ac-103">Publicar o serviço atual para o Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="ae5ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae5ac-104">SYNTAX</span></span>

### <span data-ttu-id="ae5ac-105">PublishFromServiceDefinition (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae5ac-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ae5ac-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="ae5ac-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae5ac-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae5ac-107">DESCRIPTION</span></span>
<span data-ttu-id="ae5ac-108">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ae5ac-109">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ae5ac-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ae5ac-110">O cmdlet **Publish-AzureServiceProject** publica o serviço atual para a nuvem.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="ae5ac-111">Você pode especificar a configuração de publicação (como **assinatura** , **StorageAccountName** , **local** , **slot** ) na linha de comando ou em configurações locais por meio do cmdlet **set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="ae5ac-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="ae5ac-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae5ac-112">EXAMPLES</span></span>

### <span data-ttu-id="ae5ac-113">Exemplo 1: publicar um projeto de serviço com valores padrão</span><span class="sxs-lookup"><span data-stu-id="ae5ac-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="ae5ac-114">Este exemplo publica o serviço atual, usando as configurações de serviço atuais e o perfil de publicação atual do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="ae5ac-115">Exemplo 2: criar um pacote de implantação</span><span class="sxs-lookup"><span data-stu-id="ae5ac-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="ae5ac-116">Este exemplo cria um arquivo de pacote de implantação (. cspkg) no diretório de serviço e não publica no Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="ae5ac-117">OS</span><span class="sxs-lookup"><span data-stu-id="ae5ac-117">PARAMETERS</span></span>

### <span data-ttu-id="ae5ac-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="ae5ac-118">-AffinityGroup</span></span>
<span data-ttu-id="ae5ac-119">Especifica o grupo de afinidade que você deseja que o serviço use.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-120">-Configuração</span><span class="sxs-lookup"><span data-stu-id="ae5ac-120">-Configuration</span></span>
<span data-ttu-id="ae5ac-121">Especifica o arquivo de configuração do serviço.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="ae5ac-122">Se você especificar esse parâmetro, especifique o parâmetro *Package* .</span><span class="sxs-lookup"><span data-stu-id="ae5ac-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-123">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="ae5ac-123">-DeploymentName</span></span>
<span data-ttu-id="ae5ac-124">Especifica o nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="ae5ac-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-126">-Iniciar</span><span class="sxs-lookup"><span data-stu-id="ae5ac-126">-Launch</span></span>
<span data-ttu-id="ae5ac-127">Abre uma janela do navegador para que você possa exibir o aplicativo após a implantação.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-128">-Local</span><span class="sxs-lookup"><span data-stu-id="ae5ac-128">-Location</span></span>
<span data-ttu-id="ae5ac-129">A região na qual o aplicativo será hospedado.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="ae5ac-130">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="ae5ac-130">Possible values are:</span></span> 
  
- <span data-ttu-id="ae5ac-131">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="ae5ac-131">Anywhere Asia</span></span>
- <span data-ttu-id="ae5ac-132">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="ae5ac-132">Anywhere Europe</span></span>
- <span data-ttu-id="ae5ac-133">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="ae5ac-133">Anywhere US</span></span>
- <span data-ttu-id="ae5ac-134">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="ae5ac-134">East Asia</span></span>
- <span data-ttu-id="ae5ac-135">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="ae5ac-135">East US</span></span>
- <span data-ttu-id="ae5ac-136">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="ae5ac-136">North Central US</span></span>
- <span data-ttu-id="ae5ac-137">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="ae5ac-137">North Europe</span></span>
- <span data-ttu-id="ae5ac-138">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="ae5ac-138">South Central US</span></span>
- <span data-ttu-id="ae5ac-139">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="ae5ac-139">Southeast Asia</span></span>
- <span data-ttu-id="ae5ac-140">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="ae5ac-140">West Europe</span></span>
- <span data-ttu-id="ae5ac-141">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="ae5ac-141">West US</span></span>
 
<span data-ttu-id="ae5ac-142">Se não for especificada nenhuma localização, o local especificado na última chamada a **set-AzureServiceProject** será usado.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="ae5ac-143">Se nenhum local for especificado, o local será escolhido aleatoriamente nos locais ' centro-norte-americano ' e ' centro-sul '.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-144">-Package</span><span class="sxs-lookup"><span data-stu-id="ae5ac-144">-Package</span></span>
<span data-ttu-id="ae5ac-145">Especifica o arquivo de pacote a ser implantado.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="ae5ac-146">Especifique um arquivo local que tenha a extensão de nome de arquivo. cspkg ou um URI de um blob que contenha o pacote.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="ae5ac-147">Se você especificar esse parâmetro, não especifique o parâmetro *ServiceName* .</span><span class="sxs-lookup"><span data-stu-id="ae5ac-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-148">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ae5ac-148">-Profile</span></span>
<span data-ttu-id="ae5ac-149">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae5ac-150">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae5ac-151">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ae5ac-151">-ServiceName</span></span>
<span data-ttu-id="ae5ac-152">Especifica o nome a ser usado para o serviço durante a publicação no Windows Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="ae5ac-153">O nome determina parte da etiqueta no subdomínio cloudapp.net que é usado para endereçar o serviço quando hospedado no Windows Azure (ou seja, **Name**. cloudapp.net).</span><span class="sxs-lookup"><span data-stu-id="ae5ac-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="ae5ac-154">Qualquer nome especificado durante a publicação do serviço substitui o nome dado quando o serviço foi criado.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="ae5ac-155">(Consulte o cmdlet **New-AzureServiceProject** ).</span><span class="sxs-lookup"><span data-stu-id="ae5ac-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-156">-Slot</span><span class="sxs-lookup"><span data-stu-id="ae5ac-156">-Slot</span></span>
<span data-ttu-id="ae5ac-157">O slot de implantação a ser usado para este serviço.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="ae5ac-158">Os valores possíveis são ' preparação ' e ' produção '.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="ae5ac-159">Se nenhum slot for especificado, o slot fornecido na última chamada para Set-AzureDeploymentSlot será usado.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="ae5ac-160">Se nenhum slot for especificado, o slot ' produção ' será usado.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae5ac-161">-StorageAccountName</span></span>
<span data-ttu-id="ae5ac-162">Especifica o nome da conta de armazenamento do Windows Azure a ser usado durante a publicação do serviço.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="ae5ac-163">Esse valor não é usado até que o serviço seja publicado.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="ae5ac-164">Quando esse parâmetro não é especificado, o valor é obtido do último comando **set-AzureServiceProject** .</span><span class="sxs-lookup"><span data-stu-id="ae5ac-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="ae5ac-165">Se nenhuma conta de armazenamento for especificada, uma conta de armazenamento correspondente ao nome do serviço será usada.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="ae5ac-166">Se não houver tal conta de armazenamento, o cmdlet tentará criar uma nova.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="ae5ac-167">No entanto, a tentativa poderá falhar se uma conta de armazenamento que corresponda ao nome do serviço existir em outra assinatura.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5ac-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5ac-168">CommonParameters</span></span>
<span data-ttu-id="ae5ac-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5ac-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5ac-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5ac-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5ac-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae5ac-171">INPUTS</span></span>

## <span data-ttu-id="ae5ac-172">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae5ac-172">OUTPUTS</span></span>

## <span data-ttu-id="ae5ac-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae5ac-173">NOTES</span></span>

## <span data-ttu-id="ae5ac-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae5ac-174">RELATED LINKS</span></span>

[<span data-ttu-id="ae5ac-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="ae5ac-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="ae5ac-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ae5ac-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


