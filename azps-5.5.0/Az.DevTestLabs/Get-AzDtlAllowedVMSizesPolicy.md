---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8e4fbc28d52e8431122b8593b68b909554df6dc9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116831"
---
# <span data-ttu-id="66d68-101">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="66d68-101">Get-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="66d68-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="66d68-102">SYNOPSIS</span></span>
<span data-ttu-id="66d68-103">Obtém a política de tamanhos de máquina virtuais permitidos de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="66d68-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="66d68-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66d68-104">SYNTAX</span></span>

```
Get-AzDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66d68-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="66d68-105">DESCRIPTION</span></span>
<span data-ttu-id="66d68-106">O cmdlet **Get-AzDtlAllowedVMIzesPolicy** obtém a política de tamanhos de máquina virtuais permitidos, que permite especificar uma lista de tamanhos de máquina virtuais permitidos no laboratório.</span><span class="sxs-lookup"><span data-stu-id="66d68-106">The **Get-AzDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="66d68-107">O cmdlet retorna o status habilitado ou desabilitado da política e uma lista de todos os tamanhos de máquina virtuais permitidos que você definiu na política especificada.</span><span class="sxs-lookup"><span data-stu-id="66d68-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="66d68-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66d68-108">EXAMPLES</span></span>

## <span data-ttu-id="66d68-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66d68-109">PARAMETERS</span></span>

### <span data-ttu-id="66d68-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66d68-110">-DefaultProfile</span></span>
<span data-ttu-id="66d68-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="66d68-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66d68-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="66d68-112">-LabName</span></span>
<span data-ttu-id="66d68-113">Especifica o nome do laboratório para o qual este cmdlet obtém a política de tamanho de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="66d68-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="66d68-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66d68-114">-ResourceGroupName</span></span>
<span data-ttu-id="66d68-115">Especifica o nome do grupo de recursos ao que o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="66d68-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="66d68-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66d68-116">CommonParameters</span></span>
<span data-ttu-id="66d68-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66d68-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66d68-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66d68-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66d68-119">Entradas</span><span class="sxs-lookup"><span data-stu-id="66d68-119">INPUTS</span></span>

### <span data-ttu-id="66d68-120">System.String</span><span class="sxs-lookup"><span data-stu-id="66d68-120">System.String</span></span>

## <span data-ttu-id="66d68-121">Saídas</span><span class="sxs-lookup"><span data-stu-id="66d68-121">OUTPUTS</span></span>

### <span data-ttu-id="66d68-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="66d68-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="66d68-123">Notas</span><span class="sxs-lookup"><span data-stu-id="66d68-123">NOTES</span></span>

## <span data-ttu-id="66d68-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="66d68-124">RELATED LINKS</span></span>

[<span data-ttu-id="66d68-125">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="66d68-125">Set-AzDtlAllowedVMSizesPolicy</span></span>](./Set-AzDtlAllowedVMSizesPolicy.md)


