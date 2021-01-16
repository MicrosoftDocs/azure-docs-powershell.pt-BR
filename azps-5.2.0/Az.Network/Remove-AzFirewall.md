---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260293"
---
# <span data-ttu-id="23993-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="23993-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="23993-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23993-102">SYNOPSIS</span></span>
<span data-ttu-id="23993-103">Remover um firewall.</span><span class="sxs-lookup"><span data-stu-id="23993-103">Remove a Firewall.</span></span>

## <span data-ttu-id="23993-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23993-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23993-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23993-105">DESCRIPTION</span></span>
<span data-ttu-id="23993-106">O cmdlet **Remove-AzFirewall** remove um firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="23993-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="23993-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23993-107">EXAMPLES</span></span>

### <span data-ttu-id="23993-108">Exemplo 1: criar e excluir um firewall</span><span class="sxs-lookup"><span data-stu-id="23993-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="23993-109">Este exemplo cria um firewall e, em seguida, o exclui.</span><span class="sxs-lookup"><span data-stu-id="23993-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="23993-110">Para suprimir o prompt ao excluir o firewall, use o sinalizador-Force.</span><span class="sxs-lookup"><span data-stu-id="23993-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="23993-111">OS</span><span class="sxs-lookup"><span data-stu-id="23993-111">PARAMETERS</span></span>

### <span data-ttu-id="23993-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23993-112">-AsJob</span></span>
<span data-ttu-id="23993-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="23993-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23993-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23993-114">-DefaultProfile</span></span>
<span data-ttu-id="23993-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23993-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23993-116">-Force</span><span class="sxs-lookup"><span data-stu-id="23993-116">-Force</span></span>
<span data-ttu-id="23993-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="23993-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23993-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="23993-118">-Name</span></span>
<span data-ttu-id="23993-119">Especifica o nome do firewall que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="23993-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="23993-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23993-120">-PassThru</span></span>
<span data-ttu-id="23993-121">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="23993-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="23993-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="23993-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23993-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23993-123">-ResourceGroupName</span></span>
<span data-ttu-id="23993-124">Especifica o nome do grupo de recursos que contém o firewall que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="23993-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="23993-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="23993-125">-Confirm</span></span>
<span data-ttu-id="23993-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23993-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23993-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23993-127">-WhatIf</span></span>
<span data-ttu-id="23993-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="23993-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23993-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="23993-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23993-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23993-130">CommonParameters</span></span>
<span data-ttu-id="23993-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23993-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23993-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23993-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23993-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23993-133">INPUTS</span></span>

### <span data-ttu-id="23993-134">System. String</span><span class="sxs-lookup"><span data-stu-id="23993-134">System.String</span></span>

## <span data-ttu-id="23993-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23993-135">OUTPUTS</span></span>

### <span data-ttu-id="23993-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23993-136">System.Boolean</span></span>

## <span data-ttu-id="23993-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23993-137">NOTES</span></span>

## <span data-ttu-id="23993-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23993-138">RELATED LINKS</span></span>

[<span data-ttu-id="23993-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="23993-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="23993-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="23993-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="23993-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="23993-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
