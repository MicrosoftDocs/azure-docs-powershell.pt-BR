---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112790"
---
# <span data-ttu-id="dabad-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dabad-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="dabad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dabad-102">SYNOPSIS</span></span>
<span data-ttu-id="dabad-103">Remover um Firewall.</span><span class="sxs-lookup"><span data-stu-id="dabad-103">Remove a Firewall.</span></span>

## <span data-ttu-id="dabad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dabad-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dabad-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="dabad-105">DESCRIPTION</span></span>
<span data-ttu-id="dabad-106">O cmdlet **Remove-AzFirewall** remove um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="dabad-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="dabad-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="dabad-107">EXAMPLES</span></span>

### <span data-ttu-id="dabad-108">Exemplo 1: Criar e excluir um Firewall</span><span class="sxs-lookup"><span data-stu-id="dabad-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="dabad-109">Este exemplo cria um Firewall e o exclui.</span><span class="sxs-lookup"><span data-stu-id="dabad-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="dabad-110">Para suprimir o prompt ao excluir o Firewall, use o sinalizador -Force.</span><span class="sxs-lookup"><span data-stu-id="dabad-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="dabad-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dabad-111">PARAMETERS</span></span>

### <span data-ttu-id="dabad-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dabad-112">-AsJob</span></span>
<span data-ttu-id="dabad-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dabad-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dabad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabad-114">-DefaultProfile</span></span>
<span data-ttu-id="dabad-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="dabad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dabad-116">-Forçar</span><span class="sxs-lookup"><span data-stu-id="dabad-116">-Force</span></span>
<span data-ttu-id="dabad-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="dabad-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dabad-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dabad-118">-Name</span></span>
<span data-ttu-id="dabad-119">Especifica o nome do firewall que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="dabad-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabad-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dabad-120">-PassThru</span></span>
<span data-ttu-id="dabad-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="dabad-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dabad-122">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="dabad-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dabad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabad-123">-ResourceGroupName</span></span>
<span data-ttu-id="dabad-124">Especifica o nome do grupo de recursos que contém o firewall que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="dabad-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabad-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="dabad-125">-Confirm</span></span>
<span data-ttu-id="dabad-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dabad-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dabad-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dabad-127">-WhatIf</span></span>
<span data-ttu-id="dabad-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="dabad-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dabad-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dabad-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dabad-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabad-130">CommonParameters</span></span>
<span data-ttu-id="dabad-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabad-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabad-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabad-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabad-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="dabad-133">INPUTS</span></span>

### <span data-ttu-id="dabad-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dabad-134">System.String</span></span>

## <span data-ttu-id="dabad-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="dabad-135">OUTPUTS</span></span>

### <span data-ttu-id="dabad-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dabad-136">System.Boolean</span></span>

## <span data-ttu-id="dabad-137">Notas</span><span class="sxs-lookup"><span data-stu-id="dabad-137">NOTES</span></span>

## <span data-ttu-id="dabad-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dabad-138">RELATED LINKS</span></span>

[<span data-ttu-id="dabad-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dabad-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="dabad-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dabad-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="dabad-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dabad-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
