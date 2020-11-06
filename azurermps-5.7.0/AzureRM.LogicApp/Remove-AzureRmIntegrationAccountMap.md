---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 769a92f9cd164ef2b3754a84d7a948f3bedd05da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428194"
---
# <span data-ttu-id="a3d06-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a3d06-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="a3d06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3d06-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d06-103">Remove um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a3d06-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3d06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3d06-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3d06-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3d06-105">DESCRIPTION</span></span>
<span data-ttu-id="a3d06-106">O cmdlet **Remove-AzureRmIntegrationAccountMap** remove um mapa de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3d06-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="a3d06-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do mapa.</span><span class="sxs-lookup"><span data-stu-id="a3d06-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="a3d06-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="a3d06-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a3d06-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="a3d06-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a3d06-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a3d06-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a3d06-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="a3d06-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a3d06-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3d06-112">EXAMPLES</span></span>

### <span data-ttu-id="a3d06-113">Exemplo 1: remover um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="a3d06-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="a3d06-114">Esse comando Remove o mapa da conta de integração chamado IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="a3d06-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="a3d06-115">OS</span><span class="sxs-lookup"><span data-stu-id="a3d06-115">PARAMETERS</span></span>

### <span data-ttu-id="a3d06-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d06-116">-DefaultProfile</span></span>
<span data-ttu-id="a3d06-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a3d06-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3d06-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a3d06-118">-Force</span></span>
<span data-ttu-id="a3d06-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a3d06-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a3d06-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="a3d06-120">-MapName</span></span>
<span data-ttu-id="a3d06-121">Especifica o nome do mapa da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a3d06-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d06-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3d06-122">-Name</span></span>
<span data-ttu-id="a3d06-123">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a3d06-123">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3d06-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3d06-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3d06-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a3d06-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a3d06-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3d06-126">-Confirm</span></span>
<span data-ttu-id="a3d06-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3d06-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3d06-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3d06-128">-WhatIf</span></span>
<span data-ttu-id="a3d06-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3d06-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3d06-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3d06-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3d06-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d06-131">CommonParameters</span></span>
<span data-ttu-id="a3d06-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d06-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d06-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3d06-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d06-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3d06-134">INPUTS</span></span>

### <span data-ttu-id="a3d06-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a3d06-135">None</span></span>
<span data-ttu-id="a3d06-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="a3d06-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a3d06-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3d06-137">OUTPUTS</span></span>

## <span data-ttu-id="a3d06-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3d06-138">NOTES</span></span>

## <span data-ttu-id="a3d06-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3d06-139">RELATED LINKS</span></span>

[<span data-ttu-id="a3d06-140">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a3d06-140">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="a3d06-141">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a3d06-141">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="a3d06-142">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="a3d06-142">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


