---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 13140b5434cdc29754b8041a32f328e0b855fed2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263160"
---
# <span data-ttu-id="02867-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="02867-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="02867-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02867-102">SYNOPSIS</span></span>
<span data-ttu-id="02867-103">Remove um manipulador de extensão DSC de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02867-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="02867-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02867-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02867-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="02867-105">DESCRIPTION</span></span>
<span data-ttu-id="02867-106">O cmdlet **Remove-AzVMDscExtension** remove um manipulador de extensão de configuração de estado desejado (DSC) de uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02867-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="02867-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02867-107">EXAMPLES</span></span>

### <span data-ttu-id="02867-108">Exemplo 1: remover uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="02867-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="02867-109">Esse comando Remove a extensão nomeada DSC na máquina virtual chamada VM07.</span><span class="sxs-lookup"><span data-stu-id="02867-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="02867-110">OS</span><span class="sxs-lookup"><span data-stu-id="02867-110">PARAMETERS</span></span>

### <span data-ttu-id="02867-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02867-111">-DefaultProfile</span></span>
<span data-ttu-id="02867-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02867-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02867-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="02867-113">-Name</span></span>
<span data-ttu-id="02867-114">Especifica o nome da extensão DSC que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="02867-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="02867-115">O cmdlet Set-AzVMDscExtension define esse nome como Microsoft. PowerShell. DSC, que é o valor padrão usado pelo **Remove-AzVMDscExtension**.</span><span class="sxs-lookup"><span data-stu-id="02867-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02867-116">-Nowait</span><span class="sxs-lookup"><span data-stu-id="02867-116">-NoWait</span></span>
<span data-ttu-id="02867-117">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="02867-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="02867-118">Para determinar se a operação foi concluída com êxito, use outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="02867-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02867-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02867-119">-ResourceGroupName</span></span>
<span data-ttu-id="02867-120">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="02867-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="02867-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="02867-121">-VMName</span></span>
<span data-ttu-id="02867-122">Especifica o nome de uma máquina virtual a partir da qual esse cmdlet Remove a extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="02867-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="02867-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="02867-123">-Confirm</span></span>
<span data-ttu-id="02867-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02867-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02867-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02867-125">-WhatIf</span></span>
<span data-ttu-id="02867-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="02867-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02867-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="02867-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02867-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02867-128">CommonParameters</span></span>
<span data-ttu-id="02867-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02867-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02867-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02867-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02867-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="02867-131">INPUTS</span></span>

### <span data-ttu-id="02867-132">System. String</span><span class="sxs-lookup"><span data-stu-id="02867-132">System.String</span></span>

## <span data-ttu-id="02867-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="02867-133">OUTPUTS</span></span>

### <span data-ttu-id="02867-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="02867-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="02867-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="02867-135">NOTES</span></span>

## <span data-ttu-id="02867-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02867-136">RELATED LINKS</span></span>

[<span data-ttu-id="02867-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="02867-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="02867-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="02867-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


