---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946497"
---
# <span data-ttu-id="c92bd-101">Remove-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c92bd-101">Remove-AzureApplicationGateway</span></span>

## <span data-ttu-id="c92bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c92bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c92bd-103">Remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c92bd-103">Removes an application gateway.</span></span>

## <span data-ttu-id="c92bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c92bd-104">SYNTAX</span></span>

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c92bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c92bd-105">DESCRIPTION</span></span>
<span data-ttu-id="c92bd-106">O cmdlet **Remove-AzureApplicationGateway** remove um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c92bd-106">The **Remove-AzureApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="c92bd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c92bd-107">EXAMPLES</span></span>

### <span data-ttu-id="c92bd-108">Exemplo 1: remover um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c92bd-108">Example 1: Remove an application gateway</span></span>
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

<span data-ttu-id="c92bd-109">Esse comando Remove o Application Gateway chamado ApplicationGateway06.</span><span class="sxs-lookup"><span data-stu-id="c92bd-109">This command removes the application gateway named ApplicationGateway06.</span></span>

## <span data-ttu-id="c92bd-110">OS</span><span class="sxs-lookup"><span data-stu-id="c92bd-110">PARAMETERS</span></span>

### <span data-ttu-id="c92bd-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="c92bd-111">-Name</span></span>
<span data-ttu-id="c92bd-112">Especifica o nome do gateway do aplicativo que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c92bd-112">Specifies the name of the application gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c92bd-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c92bd-113">-Profile</span></span>
<span data-ttu-id="c92bd-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c92bd-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c92bd-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c92bd-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c92bd-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c92bd-116">CommonParameters</span></span>
<span data-ttu-id="c92bd-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c92bd-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c92bd-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c92bd-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c92bd-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c92bd-119">INPUTS</span></span>

### <span data-ttu-id="c92bd-120">System. String</span><span class="sxs-lookup"><span data-stu-id="c92bd-120">System.String</span></span>

## <span data-ttu-id="c92bd-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c92bd-121">OUTPUTS</span></span>

### <span data-ttu-id="c92bd-122">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c92bd-122">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="c92bd-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c92bd-123">NOTES</span></span>

## <span data-ttu-id="c92bd-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c92bd-124">RELATED LINKS</span></span>

[<span data-ttu-id="c92bd-125">Get-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c92bd-125">Get-AzureApplicationGateway</span></span>](./Get-AzureApplicationGateway.md)

[<span data-ttu-id="c92bd-126">New-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c92bd-126">New-AzureApplicationGateway</span></span>](./New-AzureApplicationGateway.md)

[<span data-ttu-id="c92bd-127">Start-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c92bd-127">Start-AzureApplicationGateway</span></span>](./Start-AzureApplicationGateway.md)

[<span data-ttu-id="c92bd-128">Parar-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c92bd-128">Stop-AzureApplicationGateway</span></span>](./Stop-AzureApplicationGateway.md)

[<span data-ttu-id="c92bd-129">Update-AzureApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c92bd-129">Update-AzureApplicationGateway</span></span>](./Update-AzureApplicationGateway.md)


