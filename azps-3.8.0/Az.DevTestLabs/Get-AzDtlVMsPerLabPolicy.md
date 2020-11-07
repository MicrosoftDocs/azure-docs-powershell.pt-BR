---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 29d887639dd88f85a24144a4482c40c2b7626c7e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942359"
---
# <span data-ttu-id="a9f90-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a9f90-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="a9f90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9f90-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f90-103">Obtém a política de máquinas virtuais por laboratório de um laboratório no DevTest Labs.</span><span class="sxs-lookup"><span data-stu-id="a9f90-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="a9f90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9f90-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f90-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9f90-105">DESCRIPTION</span></span>
<span data-ttu-id="a9f90-106">O cmdlet **Get-AzDtlVMsPerLabPolicy** Obtém as máquinas virtuais por política de laboratório de um laboratório, que permite definir o número total de máquinas virtuais permitidas em um laboratório.</span><span class="sxs-lookup"><span data-stu-id="a9f90-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="a9f90-107">O cmdlet retorna o status habilitado ou desabilitado da política e o número total de máquinas virtuais permitidas no laboratório que você definiu na política.</span><span class="sxs-lookup"><span data-stu-id="a9f90-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="a9f90-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9f90-108">EXAMPLES</span></span>

## <span data-ttu-id="a9f90-109">OS</span><span class="sxs-lookup"><span data-stu-id="a9f90-109">PARAMETERS</span></span>

### <span data-ttu-id="a9f90-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f90-110">-DefaultProfile</span></span>
<span data-ttu-id="a9f90-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9f90-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9f90-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a9f90-112">-LabName</span></span>
<span data-ttu-id="a9f90-113">Especifica o nome do laboratório para o qual esse cmdlet obtém as máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="a9f90-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="a9f90-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f90-114">-ResourceGroupName</span></span>
<span data-ttu-id="a9f90-115">Especifica o nome do grupo de recursos ao qual o laboratório pertence.</span><span class="sxs-lookup"><span data-stu-id="a9f90-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a9f90-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f90-116">CommonParameters</span></span>
<span data-ttu-id="a9f90-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f90-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f90-118">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9f90-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f90-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9f90-119">INPUTS</span></span>

### <span data-ttu-id="a9f90-120">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f90-120">System.String</span></span>

## <span data-ttu-id="a9f90-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9f90-121">OUTPUTS</span></span>

### <span data-ttu-id="a9f90-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a9f90-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a9f90-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9f90-123">NOTES</span></span>

## <span data-ttu-id="a9f90-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9f90-124">RELATED LINKS</span></span>

[<span data-ttu-id="a9f90-125">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a9f90-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


