---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776916"
---
# <span data-ttu-id="8adbe-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8adbe-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="8adbe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8adbe-102">SYNOPSIS</span></span>
<span data-ttu-id="8adbe-103">Remove uma extensão de script personalizada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8adbe-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="8adbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8adbe-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8adbe-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8adbe-105">DESCRIPTION</span></span>
<span data-ttu-id="8adbe-106">O cmdlet **Remove-AzVMCustomScriptExtension** remove uma extensão de máquina virtual de script personalizada de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8adbe-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="8adbe-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8adbe-107">EXAMPLES</span></span>

## <span data-ttu-id="8adbe-108">OS</span><span class="sxs-lookup"><span data-stu-id="8adbe-108">PARAMETERS</span></span>

### <span data-ttu-id="8adbe-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8adbe-109">-DefaultProfile</span></span>
<span data-ttu-id="8adbe-110">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8adbe-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8adbe-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8adbe-111">-Force</span></span>
<span data-ttu-id="8adbe-112">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8adbe-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8adbe-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8adbe-113">-Name</span></span>
<span data-ttu-id="8adbe-114">Especifica o nome da extensão de script personalizada que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="8adbe-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8adbe-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8adbe-115">-ResourceGroupName</span></span>
<span data-ttu-id="8adbe-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8adbe-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8adbe-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="8adbe-117">-VMName</span></span>
<span data-ttu-id="8adbe-118">Especifica o nome de uma máquina virtual a partir da qual esse cmdlet Remove a extensão de script personalizada.</span><span class="sxs-lookup"><span data-stu-id="8adbe-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="8adbe-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8adbe-119">-Confirm</span></span>
<span data-ttu-id="8adbe-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8adbe-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8adbe-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8adbe-121">-WhatIf</span></span>
<span data-ttu-id="8adbe-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8adbe-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="8adbe-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8adbe-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8adbe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8adbe-124">CommonParameters</span></span>
<span data-ttu-id="8adbe-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8adbe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8adbe-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8adbe-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8adbe-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8adbe-127">INPUTS</span></span>

### <span data-ttu-id="8adbe-128">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8adbe-128">None</span></span>
<span data-ttu-id="8adbe-129">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8adbe-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8adbe-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8adbe-130">OUTPUTS</span></span>

### <span data-ttu-id="8adbe-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8adbe-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8adbe-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8adbe-132">NOTES</span></span>

## <span data-ttu-id="8adbe-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8adbe-133">RELATED LINKS</span></span>

[<span data-ttu-id="8adbe-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8adbe-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="8adbe-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="8adbe-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
