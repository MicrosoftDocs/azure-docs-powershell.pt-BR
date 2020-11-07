---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946429"
---
# <span data-ttu-id="497cc-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="497cc-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="497cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="497cc-102">SYNOPSIS</span></span>
<span data-ttu-id="497cc-103">Configura um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="497cc-103">Configures an application gateway.</span></span>

## <span data-ttu-id="497cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="497cc-104">SYNTAX</span></span>

### <span data-ttu-id="497cc-105">ConfigFile</span><span class="sxs-lookup"><span data-stu-id="497cc-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="497cc-106">configobject</span><span class="sxs-lookup"><span data-stu-id="497cc-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="497cc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="497cc-107">DESCRIPTION</span></span>
<span data-ttu-id="497cc-108">O cmdlet **set-AzureApplicationGatewayConfig** configura um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="497cc-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="497cc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="497cc-109">EXAMPLES</span></span>

### <span data-ttu-id="497cc-110">Exemplo 1: configurar um gateway de aplicativo usando um objeto de configuração</span><span class="sxs-lookup"><span data-stu-id="497cc-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="497cc-111">O primeiro comando obtém o objeto de configuração para o gateway do aplicativo chamado ApplicationGateway02 usando o cmdlet **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="497cc-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="497cc-112">O comando o armazena na variável $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="497cc-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="497cc-113">O segundo comando define a configuração do aplicativo chamado ApplicationGateway06 usando um objeto de configuração do Application Gateway armazenado na variável $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="497cc-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="497cc-114">Exemplo 2: configurar um gateway de aplicativo usando um arquivo de configuração</span><span class="sxs-lookup"><span data-stu-id="497cc-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="497cc-115">Esse comando define a configuração do aplicativo chamado ApplicationGateway06 usando um arquivo de configuração de gateway do aplicativo no local especificado.</span><span class="sxs-lookup"><span data-stu-id="497cc-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="497cc-116">Exemplo 3: modificar uma configuração usando um objeto de configuração</span><span class="sxs-lookup"><span data-stu-id="497cc-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="497cc-117">O primeiro comando obtém o objeto de configuração para o gateway do aplicativo chamado ApplicationGateway06 usando o cmdlet **Get-AzureApplicationGatewayConfig** .</span><span class="sxs-lookup"><span data-stu-id="497cc-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="497cc-118">O comando o armazena na variável $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="497cc-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="497cc-119">O segundo comando atribui um valor de porta a uma propriedade de **porta** no objeto armazenado em $ConfigReturnObject.</span><span class="sxs-lookup"><span data-stu-id="497cc-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="497cc-120">O comando final passa o $ConfigReturnObject atualizado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="497cc-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="497cc-121">OS</span><span class="sxs-lookup"><span data-stu-id="497cc-121">PARAMETERS</span></span>

### <span data-ttu-id="497cc-122">-Config</span><span class="sxs-lookup"><span data-stu-id="497cc-122">-Config</span></span>
<span data-ttu-id="497cc-123">Especifica um objeto de configuração de gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="497cc-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="497cc-124">Esse cmdlet atribui a configuração que esse parâmetro especifica a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="497cc-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497cc-125">-ConfigFile</span><span class="sxs-lookup"><span data-stu-id="497cc-125">-ConfigFile</span></span>
<span data-ttu-id="497cc-126">Especifica o caminho de um arquivo de configuração, em formato XML, para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="497cc-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="497cc-127">Esse cmdlet atribui a configuração que esse parâmetro especifica a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="497cc-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="497cc-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="497cc-128">-Name</span></span>
<span data-ttu-id="497cc-129">Especifica o nome do gateway do aplicativo que este cmdlet configura.</span><span class="sxs-lookup"><span data-stu-id="497cc-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="497cc-130">-Perfil</span><span class="sxs-lookup"><span data-stu-id="497cc-130">-Profile</span></span>
<span data-ttu-id="497cc-131">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="497cc-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="497cc-132">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="497cc-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="497cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="497cc-133">CommonParameters</span></span>
<span data-ttu-id="497cc-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="497cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="497cc-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="497cc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="497cc-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="497cc-136">INPUTS</span></span>

### <span data-ttu-id="497cc-137">System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="497cc-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="497cc-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="497cc-138">OUTPUTS</span></span>

### <span data-ttu-id="497cc-139">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="497cc-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="497cc-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="497cc-140">NOTES</span></span>

## <span data-ttu-id="497cc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="497cc-141">RELATED LINKS</span></span>

[<span data-ttu-id="497cc-142">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="497cc-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


