---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 2ec4ec1898e79fd7f7f35a406f2a99f9dd2da6fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597457"
---
# <span data-ttu-id="b98e7-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b98e7-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="b98e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b98e7-102">SYNOPSIS</span></span>
<span data-ttu-id="b98e7-103">Obtém informações sobre uma extensão de domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="b98e7-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="b98e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b98e7-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b98e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b98e7-105">DESCRIPTION</span></span>
<span data-ttu-id="b98e7-106">O cmdlet **Get-AzVMADDomainExtension** Obtém informações sobre a extensão de domínio do Azure Active Directory (AD) especificada.</span><span class="sxs-lookup"><span data-stu-id="b98e7-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="b98e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b98e7-107">EXAMPLES</span></span>

## <span data-ttu-id="b98e7-108">OS</span><span class="sxs-lookup"><span data-stu-id="b98e7-108">PARAMETERS</span></span>

### <span data-ttu-id="b98e7-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b98e7-109">-DefaultProfile</span></span>
<span data-ttu-id="b98e7-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b98e7-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b98e7-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="b98e7-111">-Name</span></span>
<span data-ttu-id="b98e7-112">Especifica o nome da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="b98e7-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="b98e7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b98e7-113">-ResourceGroupName</span></span>
<span data-ttu-id="b98e7-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b98e7-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b98e7-115">-Status</span><span class="sxs-lookup"><span data-stu-id="b98e7-115">-Status</span></span>
<span data-ttu-id="b98e7-116">Indica que esse cmdlet obtém o modo de exibição de instância da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="b98e7-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="b98e7-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="b98e7-117">-VMName</span></span>
<span data-ttu-id="b98e7-118">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b98e7-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="b98e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b98e7-119">CommonParameters</span></span>
<span data-ttu-id="b98e7-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b98e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b98e7-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b98e7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b98e7-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b98e7-122">INPUTS</span></span>

### <span data-ttu-id="b98e7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b98e7-123">System.String</span></span>

### <span data-ttu-id="b98e7-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b98e7-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b98e7-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b98e7-125">OUTPUTS</span></span>

### <span data-ttu-id="b98e7-126">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="b98e7-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="b98e7-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b98e7-127">NOTES</span></span>

## <span data-ttu-id="b98e7-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b98e7-128">RELATED LINKS</span></span>

[<span data-ttu-id="b98e7-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="b98e7-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


