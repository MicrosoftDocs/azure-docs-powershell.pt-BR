---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 607FBE75-727D-4388-9504-94AD31BCDBBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccount.md
ms.openlocfilehash: eb78395274171f448076a4cd3ad9b6bac0093301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93611106"
---
# <span data-ttu-id="5c4eb-101">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5c4eb-101">Remove-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="5c4eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4eb-103">Remove uma conta de integração.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-103">Removes an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c4eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c4eb-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c4eb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c4eb-105">DESCRIPTION</span></span>
<span data-ttu-id="5c4eb-106">O cmdlet **Remove-AzureRmIntegrationAccount** remove uma conta de integração de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-106">The **Remove-AzureRmIntegrationAccount** cmdlet removes an integration account from a resource group.</span></span>
<span data-ttu-id="5c4eb-107">Especifique o nome da conta de integração e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-107">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="5c4eb-108">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5c4eb-109">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5c4eb-110">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5c4eb-111">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5c4eb-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c4eb-112">EXAMPLES</span></span>

### <span data-ttu-id="5c4eb-113">Exemplo 1: remover uma conta de integração</span><span class="sxs-lookup"><span data-stu-id="5c4eb-113">Example 1: Remove an integration account</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Force
```

<span data-ttu-id="5c4eb-114">Esse comando Remove uma conta de integração chamada IntegrationAccount31.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-114">This command removes an integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="5c4eb-115">OS</span><span class="sxs-lookup"><span data-stu-id="5c4eb-115">PARAMETERS</span></span>

### <span data-ttu-id="5c4eb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5c4eb-116">-Force</span></span>
<span data-ttu-id="5c4eb-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c4eb-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c4eb-118">-Name</span></span>
<span data-ttu-id="5c4eb-119">Especifica o nome da conta de integração.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-119">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="5c4eb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c4eb-120">-ResourceGroupName</span></span>
<span data-ttu-id="5c4eb-121">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-121">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5c4eb-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c4eb-122">-Confirm</span></span>
<span data-ttu-id="5c4eb-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c4eb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4eb-124">-WhatIf</span></span>
<span data-ttu-id="5c4eb-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4eb-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c4eb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c4eb-127">-DefaultProfile</span></span>
<span data-ttu-id="5c4eb-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c4eb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4eb-129">CommonParameters</span></span>
<span data-ttu-id="5c4eb-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4eb-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c4eb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4eb-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c4eb-132">INPUTS</span></span>

## <span data-ttu-id="5c4eb-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c4eb-133">OUTPUTS</span></span>

## <span data-ttu-id="5c4eb-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c4eb-134">NOTES</span></span>

## <span data-ttu-id="5c4eb-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c4eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="5c4eb-136">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5c4eb-136">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="5c4eb-137">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5c4eb-137">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)

[<span data-ttu-id="5c4eb-138">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="5c4eb-138">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)


