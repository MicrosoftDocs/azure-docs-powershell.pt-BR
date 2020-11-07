---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D50984B7-FD97-4713-8E56-1C06D2B008E3
online version: ''
schema: 2.0.0
ms.openlocfilehash: a01d59d6a0755b3763eaef9b7532326ca0ffd402
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945779"
---
# <span data-ttu-id="aa04e-101">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa04e-101">Start-AzureApplicationGateway</span></span>

## <span data-ttu-id="aa04e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="aa04e-102">SYNOPSIS</span></span>
<span data-ttu-id="aa04e-103">Inicia um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa04e-103">Starts an application gateway.</span></span>

## <span data-ttu-id="aa04e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aa04e-104">SYNTAX</span></span>

```
Start-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aa04e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="aa04e-105">DESCRIPTION</span></span>
<span data-ttu-id="aa04e-106">O cmdlet **Start-AzureApplicationGateway** inicia um gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa04e-106">The **Start-AzureApplicationGateway** cmdlet starts an application gateway.</span></span>

## <span data-ttu-id="aa04e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aa04e-107">EXAMPLES</span></span>

### <span data-ttu-id="aa04e-108">Exemplo 1: iniciar um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="aa04e-108">Example 1: Start an application gateway</span></span>
```
PS C:\> Start-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="aa04e-109">Esse comando inicia o aplicativo gateway chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="aa04e-109">This command starts the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="aa04e-110">OS</span><span class="sxs-lookup"><span data-stu-id="aa04e-110">PARAMETERS</span></span>

### <span data-ttu-id="aa04e-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa04e-111">-Name</span></span>
<span data-ttu-id="aa04e-112">Especifica o nome do gateway do aplicativo que este cmdlet iniciará.</span><span class="sxs-lookup"><span data-stu-id="aa04e-112">Specifies the name of the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="aa04e-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="aa04e-113">-Profile</span></span>
<span data-ttu-id="aa04e-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="aa04e-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="aa04e-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="aa04e-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aa04e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa04e-116">CommonParameters</span></span>
<span data-ttu-id="aa04e-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa04e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa04e-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa04e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa04e-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="aa04e-119">INPUTS</span></span>

### <span data-ttu-id="aa04e-120">System. String</span><span class="sxs-lookup"><span data-stu-id="aa04e-120">System.String</span></span>

## <span data-ttu-id="aa04e-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="aa04e-121">OUTPUTS</span></span>

### <span data-ttu-id="aa04e-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aa04e-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="aa04e-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="aa04e-123">NOTES</span></span>

## <span data-ttu-id="aa04e-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aa04e-124">RELATED LINKS</span></span>

[<span data-ttu-id="aa04e-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa04e-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="aa04e-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa04e-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="aa04e-127">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa04e-127">Remove-AzureApplicationGateway</span></span>](./Remove-AzureApplicationGateway.md)

[<span data-ttu-id="aa04e-128">Parar-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa04e-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="aa04e-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aa04e-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


