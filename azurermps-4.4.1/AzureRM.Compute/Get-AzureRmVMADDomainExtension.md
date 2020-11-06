---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: e4431b657c72a82f1316f5eb8b74f45fac0f04aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428268"
---
# <span data-ttu-id="f44d3-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f44d3-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="f44d3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f44d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f44d3-103">Obtém informações sobre uma extensão de domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="f44d3-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f44d3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f44d3-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f44d3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f44d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f44d3-106">O cmdlet **Get-AzureRmVMADDomainExtension** Obtém informações sobre a extensão de domínio do Azure Active Directory (AD) especificada.</span><span class="sxs-lookup"><span data-stu-id="f44d3-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="f44d3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f44d3-107">EXAMPLES</span></span>

## <span data-ttu-id="f44d3-108">OS</span><span class="sxs-lookup"><span data-stu-id="f44d3-108">PARAMETERS</span></span>

### <span data-ttu-id="f44d3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f44d3-109">-DefaultProfile</span></span>
<span data-ttu-id="f44d3-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f44d3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f44d3-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="f44d3-111">-Name</span></span>
<span data-ttu-id="f44d3-112">Especifica o nome da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="f44d3-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44d3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f44d3-113">-ResourceGroupName</span></span>
<span data-ttu-id="f44d3-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f44d3-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f44d3-115">-Status</span><span class="sxs-lookup"><span data-stu-id="f44d3-115">-Status</span></span>
<span data-ttu-id="f44d3-116">Indica que esse cmdlet obtém o modo de exibição de instância da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="f44d3-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44d3-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="f44d3-117">-VMName</span></span>
<span data-ttu-id="f44d3-118">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f44d3-118">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f44d3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f44d3-119">CommonParameters</span></span>
<span data-ttu-id="f44d3-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f44d3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f44d3-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f44d3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f44d3-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f44d3-122">INPUTS</span></span>

## <span data-ttu-id="f44d3-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f44d3-123">OUTPUTS</span></span>

## <span data-ttu-id="f44d3-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f44d3-124">NOTES</span></span>

## <span data-ttu-id="f44d3-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f44d3-125">RELATED LINKS</span></span>

[<span data-ttu-id="f44d3-126">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="f44d3-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


