---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: fa19f45527302c858593d200fb2a6ed605d02321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888253"
---
# <span data-ttu-id="1fb40-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb40-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="1fb40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb40-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb40-103">Obtém as máquinas virtuais por política de laboratório de um laboratório em DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="1fb40-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="1fb40-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1fb40-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fb40-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1fb40-105">DESCRIPTION</span></span>
<span data-ttu-id="1fb40-106">O cmdlet **Get-AzDtlVMsPerLabPolicy** obtém as máquinas virtuais por política de laboratório de um laboratório, o que permite definir o número total de máquinas virtuais permitidas em um laboratório.</span><span class="sxs-lookup"><span data-stu-id="1fb40-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="1fb40-107">O cmdlet retorna o status habilitado ou desabilitado da política e o número total de máquinas virtuais permitidas no laboratório que você definiu na política.</span><span class="sxs-lookup"><span data-stu-id="1fb40-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="1fb40-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1fb40-108">EXAMPLES</span></span>

## <span data-ttu-id="1fb40-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1fb40-109">PARAMETERS</span></span>

### <span data-ttu-id="1fb40-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb40-110">-DefaultProfile</span></span>
<span data-ttu-id="1fb40-111">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1fb40-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1fb40-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="1fb40-112">-LabName</span></span>
<span data-ttu-id="1fb40-113">Especifica o nome do laboratório para o qual esse cmdlet obtém as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="1fb40-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="1fb40-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb40-114">-ResourceGroupName</span></span>
<span data-ttu-id="1fb40-115">Especifica o nome do grupo de recursos ao que o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="1fb40-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="1fb40-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb40-116">CommonParameters</span></span>
<span data-ttu-id="1fb40-117">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb40-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb40-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb40-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb40-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fb40-119">INPUTS</span></span>

### <span data-ttu-id="1fb40-120">System.String</span><span class="sxs-lookup"><span data-stu-id="1fb40-120">System.String</span></span>

## <span data-ttu-id="1fb40-121">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1fb40-121">OUTPUTS</span></span>

### <span data-ttu-id="1fb40-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb40-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="1fb40-123">NOTES</span><span class="sxs-lookup"><span data-stu-id="1fb40-123">NOTES</span></span>

## <span data-ttu-id="1fb40-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fb40-124">RELATED LINKS</span></span>

[<span data-ttu-id="1fb40-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb40-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


