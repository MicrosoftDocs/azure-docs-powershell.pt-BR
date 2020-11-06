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
ms.locfileid: "93601353"
---
# <span data-ttu-id="93349-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="93349-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="93349-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="93349-102">SYNOPSIS</span></span>
<span data-ttu-id="93349-103">Obtém informações sobre uma extensão de domínio do AD.</span><span class="sxs-lookup"><span data-stu-id="93349-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="93349-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93349-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93349-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="93349-105">DESCRIPTION</span></span>
<span data-ttu-id="93349-106">O cmdlet **Get-AzVMADDomainExtension** Obtém informações sobre a extensão de domínio do Azure Active Directory (AD) especificada.</span><span class="sxs-lookup"><span data-stu-id="93349-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="93349-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="93349-107">EXAMPLES</span></span>

## <span data-ttu-id="93349-108">OS</span><span class="sxs-lookup"><span data-stu-id="93349-108">PARAMETERS</span></span>

### <span data-ttu-id="93349-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93349-109">-DefaultProfile</span></span>
<span data-ttu-id="93349-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="93349-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93349-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="93349-111">-Name</span></span>
<span data-ttu-id="93349-112">Especifica o nome da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="93349-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="93349-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93349-113">-ResourceGroupName</span></span>
<span data-ttu-id="93349-114">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="93349-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="93349-115">-Status</span><span class="sxs-lookup"><span data-stu-id="93349-115">-Status</span></span>
<span data-ttu-id="93349-116">Indica que esse cmdlet obtém o modo de exibição de instância da extensão do domínio.</span><span class="sxs-lookup"><span data-stu-id="93349-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="93349-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="93349-117">-VMName</span></span>
<span data-ttu-id="93349-118">Especifica o nome da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="93349-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="93349-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93349-119">CommonParameters</span></span>
<span data-ttu-id="93349-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93349-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93349-121">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93349-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93349-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="93349-122">INPUTS</span></span>

### <span data-ttu-id="93349-123">System. String</span><span class="sxs-lookup"><span data-stu-id="93349-123">System.String</span></span>

### <span data-ttu-id="93349-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93349-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93349-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="93349-125">OUTPUTS</span></span>

### <span data-ttu-id="93349-126">Microsoft. Azure. Commands. COMPUTE. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="93349-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="93349-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="93349-127">NOTES</span></span>

## <span data-ttu-id="93349-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="93349-128">RELATED LINKS</span></span>

[<span data-ttu-id="93349-129">Set-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="93349-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


