---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 1bdad35adef15c15c77753c77533f35cfaf945ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775307"
---
# <span data-ttu-id="b7294-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7294-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="b7294-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7294-102">SYNOPSIS</span></span>
<span data-ttu-id="b7294-103">Remove um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7294-103">Removes an application security group.</span></span>

## <span data-ttu-id="b7294-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7294-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7294-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7294-105">DESCRIPTION</span></span>
<span data-ttu-id="b7294-106">O cmdlet **Remove-AzApplicationSecurityGroup** remove um grupo de segurança de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7294-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="b7294-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7294-107">EXAMPLES</span></span>

### <span data-ttu-id="b7294-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7294-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="b7294-109">Esse comando exclui um grupo de segurança de aplicativo chamado MyApplicationSecurityGrouo no grupo de recursos chamado MyResource Group.</span><span class="sxs-lookup"><span data-stu-id="b7294-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="b7294-110">OS</span><span class="sxs-lookup"><span data-stu-id="b7294-110">PARAMETERS</span></span>

### <span data-ttu-id="b7294-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7294-111">-DefaultProfile</span></span>
<span data-ttu-id="b7294-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b7294-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7294-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b7294-113">-Force</span></span>
<span data-ttu-id="b7294-114">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="b7294-114">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b7294-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7294-115">-Name</span></span>
<span data-ttu-id="b7294-116">O nome do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7294-116">The name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7294-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7294-117">-PassThru</span></span>
<span data-ttu-id="b7294-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="b7294-118">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b7294-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b7294-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7294-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7294-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7294-121">O nome do grupo de recursos do grupo de segurança do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7294-121">The resource group name of the application security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7294-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7294-122">-Confirm</span></span>
<span data-ttu-id="b7294-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7294-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7294-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7294-124">-WhatIf</span></span>
<span data-ttu-id="b7294-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b7294-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7294-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b7294-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7294-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7294-127">CommonParameters</span></span>
<span data-ttu-id="b7294-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7294-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7294-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7294-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7294-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7294-130">INPUTS</span></span>

### <span data-ttu-id="b7294-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b7294-131">System.String</span></span>

## <span data-ttu-id="b7294-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7294-132">OUTPUTS</span></span>

### <span data-ttu-id="b7294-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="b7294-133">System.Object</span></span>

## <span data-ttu-id="b7294-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7294-134">NOTES</span></span>

## <span data-ttu-id="b7294-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7294-135">RELATED LINKS</span></span>

[<span data-ttu-id="b7294-136">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7294-136">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b7294-137">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b7294-137">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
