---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 17BA2ED5-E347-45C0-AF20-CDD288469514
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07afcadb2207f2e4377601abfa6094bc3293328
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946408"
---
# <span data-ttu-id="e02d5-101">Stop-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e02d5-101">Stop-AzureApplicationGateway</span></span>

## <span data-ttu-id="e02d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e02d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e02d5-103">Interrompe um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e02d5-103">Stops an application gateway.</span></span>

## <span data-ttu-id="e02d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e02d5-104">SYNTAX</span></span>

```
Stop-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e02d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e02d5-105">DESCRIPTION</span></span>
<span data-ttu-id="e02d5-106">O cmdlet **Stop-AzureApplicationGateway** interrompe um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e02d5-106">The **Stop-AzureApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="e02d5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e02d5-107">EXAMPLES</span></span>

### <span data-ttu-id="e02d5-108">Exemplo 1: parar um gateway do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e02d5-108">Example 1: Stop an application gateway</span></span>
```
PS C:\> Stop-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="e02d5-109">Esse comando interrompe o aplicativo gateway chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="e02d5-109">This command stops the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="e02d5-110">OS</span><span class="sxs-lookup"><span data-stu-id="e02d5-110">PARAMETERS</span></span>

### <span data-ttu-id="e02d5-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="e02d5-111">-Name</span></span>
<span data-ttu-id="e02d5-112">Especifica o nome do gateway do aplicativo para o qual este cmdlet parou.</span><span class="sxs-lookup"><span data-stu-id="e02d5-112">Specifies the name of the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e02d5-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e02d5-113">-Profile</span></span>
<span data-ttu-id="e02d5-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e02d5-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e02d5-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e02d5-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e02d5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02d5-116">CommonParameters</span></span>
<span data-ttu-id="e02d5-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02d5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02d5-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02d5-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02d5-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e02d5-119">INPUTS</span></span>

### <span data-ttu-id="e02d5-120">System. String</span><span class="sxs-lookup"><span data-stu-id="e02d5-120">System.String</span></span>

## <span data-ttu-id="e02d5-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e02d5-121">OUTPUTS</span></span>

### <span data-ttu-id="e02d5-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e02d5-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="e02d5-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e02d5-123">NOTES</span></span>

## <span data-ttu-id="e02d5-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e02d5-124">RELATED LINKS</span></span>

[<span data-ttu-id="e02d5-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e02d5-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="e02d5-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e02d5-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="e02d5-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e02d5-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="e02d5-128">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e02d5-128">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="e02d5-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e02d5-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)
