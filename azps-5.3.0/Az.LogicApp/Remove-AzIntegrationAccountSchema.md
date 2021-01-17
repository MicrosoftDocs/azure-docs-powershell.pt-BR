---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98429196"
---
# <span data-ttu-id="a9678-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a9678-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="a9678-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9678-102">SYNOPSIS</span></span>
<span data-ttu-id="a9678-103">Remove um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a9678-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="a9678-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9678-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9678-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9678-105">DESCRIPTION</span></span>
<span data-ttu-id="a9678-106">O cmdlet **Remove-AzIntegrationAccountSchema** remove um esquema de conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9678-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="a9678-107">Especificando o nome da conta de integração, o nome do grupo de recursos e o nome do esquema.</span><span class="sxs-lookup"><span data-stu-id="a9678-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="a9678-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="a9678-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a9678-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="a9678-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a9678-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a9678-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a9678-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="a9678-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a9678-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9678-112">EXAMPLES</span></span>

### <span data-ttu-id="a9678-113">Exemplo 1: remover um esquema de conta de integração</span><span class="sxs-lookup"><span data-stu-id="a9678-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="a9678-114">Esse comando Remove um esquema de conta de integração chamado IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="a9678-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="a9678-115">OS</span><span class="sxs-lookup"><span data-stu-id="a9678-115">PARAMETERS</span></span>

### <span data-ttu-id="a9678-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9678-116">-DefaultProfile</span></span>
<span data-ttu-id="a9678-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9678-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9678-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a9678-118">-Force</span></span>
<span data-ttu-id="a9678-119">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a9678-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9678-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9678-120">-Name</span></span>
<span data-ttu-id="a9678-121">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a9678-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="a9678-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9678-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9678-123">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9678-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a9678-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a9678-124">-SchemaName</span></span>
<span data-ttu-id="a9678-125">Especifica o nome de um esquema de conta de integração.</span><span class="sxs-lookup"><span data-stu-id="a9678-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="a9678-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9678-126">-Confirm</span></span>
<span data-ttu-id="a9678-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9678-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9678-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9678-128">-WhatIf</span></span>
<span data-ttu-id="a9678-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9678-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9678-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9678-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9678-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9678-131">CommonParameters</span></span>
<span data-ttu-id="a9678-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9678-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9678-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9678-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9678-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9678-134">INPUTS</span></span>

### <span data-ttu-id="a9678-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a9678-135">System.String</span></span>

## <span data-ttu-id="a9678-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9678-136">OUTPUTS</span></span>

### <span data-ttu-id="a9678-137">System. void</span><span class="sxs-lookup"><span data-stu-id="a9678-137">System.Void</span></span>

## <span data-ttu-id="a9678-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9678-138">NOTES</span></span>

## <span data-ttu-id="a9678-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9678-139">RELATED LINKS</span></span>

[<span data-ttu-id="a9678-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a9678-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="a9678-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a9678-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="a9678-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a9678-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


