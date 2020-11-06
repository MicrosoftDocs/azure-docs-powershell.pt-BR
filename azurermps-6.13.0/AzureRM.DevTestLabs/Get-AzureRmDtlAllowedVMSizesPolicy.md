---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: db82ca43114a35921652424289fcc53f7761ab8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429565"
---
# <span data-ttu-id="387fe-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="387fe-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="387fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="387fe-102">SYNOPSIS</span></span>
<span data-ttu-id="387fe-103">Obtém a política de tamanhos de máquinas virtuais permitidos de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="387fe-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="387fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="387fe-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="387fe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="387fe-105">DESCRIPTION</span></span>
<span data-ttu-id="387fe-106">O cmdlet **Get-AzureRmDtlAllowedVMSizesPolicy** Obtém a política de tamanhos de máquinas virtuais permitidos, que permite que você especifique uma lista de tamanhos de máquinas virtuais permitidos no laboratório.</span><span class="sxs-lookup"><span data-stu-id="387fe-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="387fe-107">O cmdlet retorna o status habilitado ou desabilitado da política e uma lista de todos os tamanhos da máquina virtual permitidos que você definiu na política especificada.</span><span class="sxs-lookup"><span data-stu-id="387fe-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="387fe-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="387fe-108">EXAMPLES</span></span>

## <span data-ttu-id="387fe-109">OS</span><span class="sxs-lookup"><span data-stu-id="387fe-109">PARAMETERS</span></span>

### <span data-ttu-id="387fe-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387fe-110">-DefaultProfile</span></span>
<span data-ttu-id="387fe-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="387fe-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="387fe-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="387fe-112">-LabName</span></span>
<span data-ttu-id="387fe-113">Especifica o nome do laboratório para o qual este cmdlet obtém a política de tamanho de máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="387fe-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="387fe-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387fe-114">-ResourceGroupName</span></span>
<span data-ttu-id="387fe-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="387fe-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="387fe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387fe-116">CommonParameters</span></span>
<span data-ttu-id="387fe-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="387fe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387fe-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387fe-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387fe-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="387fe-119">INPUTS</span></span>

### <span data-ttu-id="387fe-120">System. String</span><span class="sxs-lookup"><span data-stu-id="387fe-120">System.String</span></span>

## <span data-ttu-id="387fe-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="387fe-121">OUTPUTS</span></span>

### <span data-ttu-id="387fe-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="387fe-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="387fe-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="387fe-123">NOTES</span></span>

## <span data-ttu-id="387fe-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="387fe-124">RELATED LINKS</span></span>

[<span data-ttu-id="387fe-125">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="387fe-125">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="387fe-126">Cmdlets de laboratório de teste do Azure Development</span><span class="sxs-lookup"><span data-stu-id="387fe-126">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)


