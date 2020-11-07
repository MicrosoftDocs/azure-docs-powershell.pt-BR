---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777039"
---
# <span data-ttu-id="5819b-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5819b-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="5819b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5819b-102">SYNOPSIS</span></span>
<span data-ttu-id="5819b-103">Obtém informações sobre uma extensão de domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="5819b-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="5819b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5819b-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5819b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5819b-105">DESCRIPTION</span></span>
<span data-ttu-id="5819b-106">O cmdlet **Get-AzVMADDomainExtension** Obtém informações sobre a extensão de domínio do Azure Active Directory (AD) especificada.</span><span class="sxs-lookup"><span data-stu-id="5819b-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="5819b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5819b-107">EXAMPLES</span></span>

### <span data-ttu-id="5819b-108">1:</span><span class="sxs-lookup"><span data-stu-id="5819b-108">1:</span></span>
```

```

## <span data-ttu-id="5819b-109">OS</span><span class="sxs-lookup"><span data-stu-id="5819b-109">PARAMETERS</span></span>

### <span data-ttu-id="5819b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5819b-110">-DefaultProfile</span></span>
<span data-ttu-id="5819b-111">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5819b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5819b-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="5819b-112">-Name</span></span>
<span data-ttu-id="5819b-113">Especifica o nome da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="5819b-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="5819b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5819b-114">-ResourceGroupName</span></span>
<span data-ttu-id="5819b-115">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5819b-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5819b-116">-Status</span><span class="sxs-lookup"><span data-stu-id="5819b-116">-Status</span></span>
<span data-ttu-id="5819b-117">Indica que esse cmdlet obtém o modo de exibição de instância da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="5819b-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="5819b-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="5819b-118">-VMName</span></span>
<span data-ttu-id="5819b-119">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5819b-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="5819b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5819b-120">CommonParameters</span></span>
<span data-ttu-id="5819b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5819b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5819b-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5819b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5819b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5819b-123">INPUTS</span></span>

### <span data-ttu-id="5819b-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5819b-124">None</span></span>
<span data-ttu-id="5819b-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5819b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5819b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5819b-126">OUTPUTS</span></span>

### <span data-ttu-id="5819b-127">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="5819b-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="5819b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5819b-128">NOTES</span></span>

## <span data-ttu-id="5819b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5819b-129">RELATED LINKS</span></span>

[<span data-ttu-id="5819b-130">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="5819b-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


