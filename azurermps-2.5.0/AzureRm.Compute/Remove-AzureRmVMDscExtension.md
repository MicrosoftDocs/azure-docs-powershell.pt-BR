---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdscextension
schema: 2.0.0
ms.openlocfilehash: f93d461bddb78230be3168cb1df534a4cde842e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785977"
---
# <span data-ttu-id="8ebfa-101">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8ebfa-101">Remove-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="8ebfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ebfa-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebfa-103">Remove um manipulador de extensão DSC de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ebfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ebfa-104">SYNTAX</span></span>

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ebfa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ebfa-105">DESCRIPTION</span></span>
<span data-ttu-id="8ebfa-106">O cmdlet **Remove-AzureRmVMDscExtension** remove um manipulador de extensão de configuração de estado desejado (DSC) de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-106">The **Remove-AzureRmVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="8ebfa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ebfa-107">EXAMPLES</span></span>

### <span data-ttu-id="8ebfa-108">Exemplo 1: remover uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="8ebfa-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="8ebfa-109">Esse comando Remove a extensão nomeada DSC na máquina virtual chamada VM07.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="8ebfa-110">OS</span><span class="sxs-lookup"><span data-stu-id="8ebfa-110">PARAMETERS</span></span>

### <span data-ttu-id="8ebfa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebfa-111">-DefaultProfile</span></span>
<span data-ttu-id="8ebfa-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ebfa-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ebfa-113">-Name</span></span>
<span data-ttu-id="8ebfa-114">Especifica o nome da extensão DSC que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="8ebfa-115">O cmdlet Set-AzureRmVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o valor padrão usado pelo **Remove-AzureRmVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-115">The Set-AzureRmVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzureRmVMDscExtension**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebfa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebfa-116">-ResourceGroupName</span></span>
<span data-ttu-id="8ebfa-117">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8ebfa-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="8ebfa-118">-VMName</span></span>
<span data-ttu-id="8ebfa-119">Especifica o nome de uma máquina virtual a partir da qual esse cmdlet Remove a extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebfa-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ebfa-120">-Confirm</span></span>
<span data-ttu-id="8ebfa-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebfa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ebfa-122">-WhatIf</span></span>
<span data-ttu-id="8ebfa-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8ebfa-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebfa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebfa-125">CommonParameters</span></span>
<span data-ttu-id="8ebfa-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebfa-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebfa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebfa-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ebfa-128">INPUTS</span></span>

### <span data-ttu-id="8ebfa-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8ebfa-129">None</span></span>
<span data-ttu-id="8ebfa-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8ebfa-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ebfa-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ebfa-131">OUTPUTS</span></span>

### <span data-ttu-id="8ebfa-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8ebfa-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8ebfa-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ebfa-133">NOTES</span></span>

## <span data-ttu-id="8ebfa-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ebfa-134">RELATED LINKS</span></span>

[<span data-ttu-id="8ebfa-135">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8ebfa-135">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="8ebfa-136">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="8ebfa-136">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


