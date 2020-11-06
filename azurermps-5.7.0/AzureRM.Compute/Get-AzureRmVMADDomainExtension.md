---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431063"
---
# <span data-ttu-id="1150f-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1150f-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="1150f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1150f-102">SYNOPSIS</span></span>
<span data-ttu-id="1150f-103">Obtém informações sobre uma extensão de domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="1150f-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1150f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1150f-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="1150f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1150f-105">DESCRIPTION</span></span>
<span data-ttu-id="1150f-106">O cmdlet **Get-AzureRmVMADDomainExtension** Obtém informações sobre a extensão de domínio do Azure Active Directory (AD) especificada.</span><span class="sxs-lookup"><span data-stu-id="1150f-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="1150f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1150f-107">EXAMPLES</span></span>

## <span data-ttu-id="1150f-108">OS</span><span class="sxs-lookup"><span data-stu-id="1150f-108">PARAMETERS</span></span>

### <span data-ttu-id="1150f-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="1150f-109">-Name</span></span>
<span data-ttu-id="1150f-110">Especifica o nome da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="1150f-110">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1150f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1150f-111">-ResourceGroupName</span></span>
<span data-ttu-id="1150f-112">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1150f-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1150f-113">-Status</span><span class="sxs-lookup"><span data-stu-id="1150f-113">-Status</span></span>
<span data-ttu-id="1150f-114">Indica que esse cmdlet obtém o modo de exibição de instância da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="1150f-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1150f-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="1150f-115">-VMName</span></span>
<span data-ttu-id="1150f-116">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1150f-116">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1150f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1150f-117">CommonParameters</span></span>
<span data-ttu-id="1150f-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1150f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1150f-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1150f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1150f-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1150f-120">INPUTS</span></span>

### <span data-ttu-id="1150f-121">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1150f-121">None</span></span>
<span data-ttu-id="1150f-122">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1150f-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1150f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1150f-123">OUTPUTS</span></span>

## <span data-ttu-id="1150f-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1150f-124">NOTES</span></span>

## <span data-ttu-id="1150f-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1150f-125">RELATED LINKS</span></span>

[<span data-ttu-id="1150f-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="1150f-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


