---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountMap.md
ms.openlocfilehash: 37e6fcbaf1347d9aec48f680de749bf0b967551a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113008"
---
# <span data-ttu-id="c8a94-101">Remove-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8a94-101">Remove-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="c8a94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8a94-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a94-103">Remove um mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c8a94-103">Removes an integration account map.</span></span>

## <span data-ttu-id="c8a94-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8a94-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a94-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8a94-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a94-106">O **cmdlet Remove-AzIntegrationAccountMap** remove um mapa de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8a94-106">The **Remove-AzIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="c8a94-107">Especifique o nome da conta de integração, o nome do grupo de recursos e o nome do mapa.</span><span class="sxs-lookup"><span data-stu-id="c8a94-107">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="c8a94-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="c8a94-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c8a94-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="c8a94-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c8a94-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c8a94-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c8a94-111">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="c8a94-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c8a94-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8a94-112">EXAMPLES</span></span>

### <span data-ttu-id="c8a94-113">Exemplo 1: Remover um mapa de conta de integração</span><span class="sxs-lookup"><span data-stu-id="c8a94-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="c8a94-114">Esse comando remove o mapa de conta de integração chamado IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="c8a94-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="c8a94-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8a94-115">PARAMETERS</span></span>

### <span data-ttu-id="c8a94-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a94-116">-DefaultProfile</span></span>
<span data-ttu-id="c8a94-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c8a94-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8a94-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="c8a94-118">-Force</span></span>
<span data-ttu-id="c8a94-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c8a94-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8a94-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="c8a94-120">-MapName</span></span>
<span data-ttu-id="c8a94-121">Especifica o nome do mapa de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c8a94-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a94-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8a94-122">-Name</span></span>
<span data-ttu-id="c8a94-123">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="c8a94-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a94-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a94-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8a94-125">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c8a94-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c8a94-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c8a94-126">-Confirm</span></span>
<span data-ttu-id="c8a94-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a94-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a94-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a94-128">-WhatIf</span></span>
<span data-ttu-id="c8a94-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c8a94-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a94-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8a94-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a94-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a94-131">CommonParameters</span></span>
<span data-ttu-id="c8a94-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a94-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a94-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a94-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a94-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8a94-134">INPUTS</span></span>

### <span data-ttu-id="c8a94-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c8a94-135">System.String</span></span>

## <span data-ttu-id="c8a94-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8a94-136">OUTPUTS</span></span>

### <span data-ttu-id="c8a94-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="c8a94-137">System.Void</span></span>

## <span data-ttu-id="c8a94-138">Notas</span><span class="sxs-lookup"><span data-stu-id="c8a94-138">NOTES</span></span>

## <span data-ttu-id="c8a94-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8a94-139">RELATED LINKS</span></span>

[<span data-ttu-id="c8a94-140">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8a94-140">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="c8a94-141">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8a94-141">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="c8a94-142">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="c8a94-142">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


