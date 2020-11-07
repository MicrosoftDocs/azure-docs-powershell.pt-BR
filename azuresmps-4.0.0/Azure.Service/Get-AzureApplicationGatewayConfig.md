---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945665"
---
# <span data-ttu-id="18d78-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="18d78-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="18d78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18d78-102">SYNOPSIS</span></span>
<span data-ttu-id="18d78-103">Obtém um contexto de configuração de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="18d78-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="18d78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18d78-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="18d78-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18d78-105">DESCRIPTION</span></span>
<span data-ttu-id="18d78-106">O cmdlet **Get-AzureApplicationGatewayConfig** Obtém um contexto de configuração do Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="18d78-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="18d78-107">Um contexto inclui um objeto de configuração e uma configuração XML.</span><span class="sxs-lookup"><span data-stu-id="18d78-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="18d78-108">Você pode salvar a configuração XML em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="18d78-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="18d78-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18d78-109">EXAMPLES</span></span>

### <span data-ttu-id="18d78-110">Exemplo 1: obter uma configuração de gateway de aplicativo e salvá-la em um arquivo</span><span class="sxs-lookup"><span data-stu-id="18d78-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="18d78-111">Esse comando obtém a configuração de um gateway de aplicativo chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="18d78-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="18d78-112">O comando salva-o no arquivo no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="18d78-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="18d78-113">OS</span><span class="sxs-lookup"><span data-stu-id="18d78-113">PARAMETERS</span></span>

### <span data-ttu-id="18d78-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="18d78-114">-ExportToFile</span></span>
<span data-ttu-id="18d78-115">Especifica um caminho de arquivo para o qual esse cmdlet salva a configuração no formato XML.</span><span class="sxs-lookup"><span data-stu-id="18d78-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18d78-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="18d78-116">-Name</span></span>
<span data-ttu-id="18d78-117">Especifica o nome do gateway do aplicativo para o qual este cmdlet obtém informações de configuração.</span><span class="sxs-lookup"><span data-stu-id="18d78-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18d78-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="18d78-118">-Profile</span></span>
<span data-ttu-id="18d78-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="18d78-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="18d78-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="18d78-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="18d78-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18d78-121">CommonParameters</span></span>
<span data-ttu-id="18d78-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18d78-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18d78-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18d78-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18d78-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18d78-124">INPUTS</span></span>

### <span data-ttu-id="18d78-125">System. String</span><span class="sxs-lookup"><span data-stu-id="18d78-125">System.String</span></span>

## <span data-ttu-id="18d78-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18d78-126">OUTPUTS</span></span>

### <span data-ttu-id="18d78-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext</span><span class="sxs-lookup"><span data-stu-id="18d78-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="18d78-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18d78-128">NOTES</span></span>

## <span data-ttu-id="18d78-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18d78-129">RELATED LINKS</span></span>

[<span data-ttu-id="18d78-130">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="18d78-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


