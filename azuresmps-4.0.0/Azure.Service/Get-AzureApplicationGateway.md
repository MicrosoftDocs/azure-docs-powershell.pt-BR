---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945670"
---
# <span data-ttu-id="5a032-101">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a032-101">Get-AzureApplicationGateway</span></span>

## <span data-ttu-id="5a032-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a032-102">SYNOPSIS</span></span>
<span data-ttu-id="5a032-103">Obtém um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5a032-103">Gets an Application Gateway.</span></span>

## <span data-ttu-id="5a032-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a032-104">SYNTAX</span></span>

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5a032-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a032-105">DESCRIPTION</span></span>
<span data-ttu-id="5a032-106">O cmdlet **Get-AzureApplicationGateway** Obtém um gateway de aplicativo do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="5a032-106">The **Get-AzureApplicationGateway** cmdlet gets an existing Azure Application Gateway.</span></span>

## <span data-ttu-id="5a032-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a032-107">EXAMPLES</span></span>

### <span data-ttu-id="5a032-108">Exemplo 1: obter um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="5a032-108">Example 1: Get an Application Gateway</span></span>
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="5a032-109">Esse comando obtém o gateway do aplicativo chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="5a032-109">This command gets the Application Gateway named ApplicationGateway06.</span></span>

### <span data-ttu-id="5a032-110">Exemplo 2: obter todos os gateways do aplicativo</span><span class="sxs-lookup"><span data-stu-id="5a032-110">Example 2: Get all Application Gateways</span></span>
```
PS C:\> Get-AzureApplicationGateway
```

<span data-ttu-id="5a032-111">Esse comando obtém todos os gateways do aplicativo em sua assinatura.</span><span class="sxs-lookup"><span data-stu-id="5a032-111">This command gets all the Application Gateways under your subscription.</span></span>

## <span data-ttu-id="5a032-112">OS</span><span class="sxs-lookup"><span data-stu-id="5a032-112">PARAMETERS</span></span>

### <span data-ttu-id="5a032-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a032-113">-Name</span></span>
<span data-ttu-id="5a032-114">Especifica o nome do aplicativo do gateway que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5a032-114">Specifies the name of the Application Gateway that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a032-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="5a032-115">-Profile</span></span>
<span data-ttu-id="5a032-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="5a032-116">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="5a032-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="5a032-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5a032-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a032-118">CommonParameters</span></span>
<span data-ttu-id="5a032-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a032-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a032-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a032-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a032-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a032-121">INPUTS</span></span>

### <span data-ttu-id="5a032-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5a032-122">System.String</span></span>

## <span data-ttu-id="5a032-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a032-123">OUTPUTS</span></span>

### <span data-ttu-id="5a032-124">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway, IEnumerable<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGateway></span><span class="sxs-lookup"><span data-stu-id="5a032-124">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway, IEnumerable<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGateway></span></span>

## <span data-ttu-id="5a032-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a032-125">NOTES</span></span>

## <span data-ttu-id="5a032-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a032-126">RELATED LINKS</span></span>

[<span data-ttu-id="5a032-127">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a032-127">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="5a032-128">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a032-128">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="5a032-129">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a032-129">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="5a032-130">Parar-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a032-130">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="5a032-131">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5a032-131">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


