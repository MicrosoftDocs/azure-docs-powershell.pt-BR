---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 4be419ab76180174fd6132335822c361008ec872
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890776"
---
# <span data-ttu-id="25905-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="25905-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="25905-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25905-102">SYNOPSIS</span></span>
<span data-ttu-id="25905-103">Remover um Firewall.</span><span class="sxs-lookup"><span data-stu-id="25905-103">Remove a Firewall.</span></span>

## <span data-ttu-id="25905-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="25905-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25905-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="25905-105">DESCRIPTION</span></span>
<span data-ttu-id="25905-106">O cmdlet **Remove-AzFirewall** remove um Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="25905-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="25905-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25905-107">EXAMPLES</span></span>

### <span data-ttu-id="25905-108">Exemplo 1: Criar e excluir um Firewall</span><span class="sxs-lookup"><span data-stu-id="25905-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="25905-109">Este exemplo cria um Firewall e o exclui.</span><span class="sxs-lookup"><span data-stu-id="25905-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="25905-110">Para suprimir o prompt ao excluir o Firewall, use o sinalizador -Force.</span><span class="sxs-lookup"><span data-stu-id="25905-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="25905-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="25905-111">PARAMETERS</span></span>

### <span data-ttu-id="25905-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25905-112">-AsJob</span></span>
<span data-ttu-id="25905-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="25905-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25905-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25905-114">-DefaultProfile</span></span>
<span data-ttu-id="25905-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="25905-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25905-116">-Force</span><span class="sxs-lookup"><span data-stu-id="25905-116">-Force</span></span>
<span data-ttu-id="25905-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="25905-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="25905-118">-Name</span><span class="sxs-lookup"><span data-stu-id="25905-118">-Name</span></span>
<span data-ttu-id="25905-119">Especifica o nome do firewall que esse cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="25905-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="25905-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25905-120">-PassThru</span></span>
<span data-ttu-id="25905-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="25905-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25905-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="25905-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25905-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25905-123">-ResourceGroupName</span></span>
<span data-ttu-id="25905-124">Especifica o nome do grupo de recursos que contém o firewall que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="25905-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="25905-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25905-125">-Confirm</span></span>
<span data-ttu-id="25905-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25905-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25905-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25905-127">-WhatIf</span></span>
<span data-ttu-id="25905-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25905-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25905-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25905-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25905-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25905-130">CommonParameters</span></span>
<span data-ttu-id="25905-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25905-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25905-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25905-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25905-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25905-133">INPUTS</span></span>

### <span data-ttu-id="25905-134">System.String</span><span class="sxs-lookup"><span data-stu-id="25905-134">System.String</span></span>

## <span data-ttu-id="25905-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="25905-135">OUTPUTS</span></span>

### <span data-ttu-id="25905-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25905-136">System.Boolean</span></span>

## <span data-ttu-id="25905-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="25905-137">NOTES</span></span>

## <span data-ttu-id="25905-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25905-138">RELATED LINKS</span></span>

[<span data-ttu-id="25905-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="25905-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="25905-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="25905-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="25905-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="25905-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
