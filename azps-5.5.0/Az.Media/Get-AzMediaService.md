---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113570"
---
# <span data-ttu-id="2c582-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2c582-101">Get-AzMediaService</span></span>

## <span data-ttu-id="2c582-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c582-102">SYNOPSIS</span></span>
<span data-ttu-id="2c582-103">Obtém informações sobre um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2c582-103">Gets information about a media service.</span></span>

## <span data-ttu-id="2c582-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c582-104">SYNTAX</span></span>

### <span data-ttu-id="2c582-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c582-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c582-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c582-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c582-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c582-107">DESCRIPTION</span></span>
<span data-ttu-id="2c582-108">O **cmdlet Get-AzMediaService** obtém informações sobre um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2c582-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="2c582-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2c582-109">EXAMPLES</span></span>

### <span data-ttu-id="2c582-110">Exemplo 1: Obter todos os serviços de mídia em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2c582-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="2c582-111">Esse comando obtém propriedades para todos os serviços de mídia no grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="2c582-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="2c582-112">Exemplo 2: Obter propriedades de serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="2c582-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="2c582-113">Esse comando obtém as propriedades do serviço de mídia chamado MediaService1 que pertence ao grupo de recursos chamado ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="2c582-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="2c582-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c582-114">PARAMETERS</span></span>

### <span data-ttu-id="2c582-115">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="2c582-115">-AccountName</span></span>
<span data-ttu-id="2c582-116">Especifica o nome do serviço de mídia que este cmdlet recebe.</span><span class="sxs-lookup"><span data-stu-id="2c582-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c582-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c582-117">-DefaultProfile</span></span>
<span data-ttu-id="2c582-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2c582-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c582-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c582-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c582-120">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2c582-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c582-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c582-121">CommonParameters</span></span>
<span data-ttu-id="2c582-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c582-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c582-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c582-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c582-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="2c582-124">INPUTS</span></span>

### <span data-ttu-id="2c582-125">System.String</span><span class="sxs-lookup"><span data-stu-id="2c582-125">System.String</span></span>

## <span data-ttu-id="2c582-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="2c582-126">OUTPUTS</span></span>

### <span data-ttu-id="2c582-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="2c582-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="2c582-128">Notas</span><span class="sxs-lookup"><span data-stu-id="2c582-128">NOTES</span></span>

## <span data-ttu-id="2c582-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c582-129">RELATED LINKS</span></span>

[<span data-ttu-id="2c582-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2c582-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="2c582-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2c582-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="2c582-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2c582-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


