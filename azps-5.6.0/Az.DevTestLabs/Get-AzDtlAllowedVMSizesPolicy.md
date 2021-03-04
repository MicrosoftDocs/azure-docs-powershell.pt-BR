---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: f1b5d95397aad24b84462c7e9ceba4a06ba854c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890859"
---
# <span data-ttu-id="ae710-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ae710-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="ae710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae710-102">SYNOPSIS</span></span>
<span data-ttu-id="ae710-103">Obtém a política de tamanhos de máquina virtual permitido de um laboratório em Laboratórios DevTest.</span><span class="sxs-lookup"><span data-stu-id="ae710-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="ae710-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae710-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae710-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae710-105">DESCRIPTION</span></span>
<span data-ttu-id="ae710-106">O cmdlet **Get-AzDtlAllowedVMSizesPolicy** obtém a política de tamanhos de máquina virtual permitidos, que permite especificar uma lista de tamanhos de máquina virtual permitidos no laboratório.</span><span class="sxs-lookup"><span data-stu-id="ae710-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="ae710-107">O cmdlet retorna o status habilitado ou desabilitado da política e uma lista de todos os tamanhos de máquina virtual permitidos que você definiu na política especificada.</span><span class="sxs-lookup"><span data-stu-id="ae710-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="ae710-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae710-108">EXAMPLES</span></span>

## <span data-ttu-id="ae710-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae710-109">PARAMETERS</span></span>

### <span data-ttu-id="ae710-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae710-110">-DefaultProfile</span></span>
<span data-ttu-id="ae710-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ae710-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae710-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="ae710-112">-LabName</span></span>
<span data-ttu-id="ae710-113">Especifica o nome do laboratório para o qual este cmdlet obtém a política de tamanho de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="ae710-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="ae710-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae710-114">-ResourceGroupName</span></span>
<span data-ttu-id="ae710-115">Especifica o nome do grupo de recursos ao que o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="ae710-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae710-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae710-116">CommonParameters</span></span>
<span data-ttu-id="ae710-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae710-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae710-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae710-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae710-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae710-119">INPUTS</span></span>

### <span data-ttu-id="ae710-120">System.String</span><span class="sxs-lookup"><span data-stu-id="ae710-120">System.String</span></span>

## <span data-ttu-id="ae710-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae710-121">OUTPUTS</span></span>

### <span data-ttu-id="ae710-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="ae710-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="ae710-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae710-123">NOTES</span></span>

## <span data-ttu-id="ae710-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae710-124">RELATED LINKS</span></span>

[<span data-ttu-id="ae710-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="ae710-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


