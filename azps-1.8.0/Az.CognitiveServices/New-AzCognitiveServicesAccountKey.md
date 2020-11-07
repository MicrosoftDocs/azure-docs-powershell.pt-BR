---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: cdc5c5252ae3f7f9a1dd59f0e56aec5a354227a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771256"
---
# <span data-ttu-id="9b8ef-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b8ef-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="9b8ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8ef-103">Regenera a chave de uma conta.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-103">Regenerates an account key.</span></span>

## <span data-ttu-id="9b8ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b8ef-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b8ef-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b8ef-105">DESCRIPTION</span></span>
<span data-ttu-id="9b8ef-106">O cmdlet **New-AzCognitiveServicesAccountKey** regenera uma chave de API para uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="9b8ef-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b8ef-107">EXAMPLES</span></span>

### <span data-ttu-id="9b8ef-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b8ef-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="9b8ef-109">OS</span><span class="sxs-lookup"><span data-stu-id="9b8ef-109">PARAMETERS</span></span>

### <span data-ttu-id="9b8ef-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8ef-110">-DefaultProfile</span></span>
<span data-ttu-id="9b8ef-111">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="9b8ef-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b8ef-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9b8ef-112">-Force</span></span>
<span data-ttu-id="9b8ef-113">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9b8ef-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="9b8ef-114">-KeyName</span></span>
<span data-ttu-id="9b8ef-115">Especifica o nome da chave a ser regenerada.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="9b8ef-116">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9b8ef-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9b8ef-117">Key1</span><span class="sxs-lookup"><span data-stu-id="9b8ef-117">Key1</span></span>
- <span data-ttu-id="9b8ef-118">Key2</span><span class="sxs-lookup"><span data-stu-id="9b8ef-118">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases:
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8ef-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b8ef-119">-Name</span></span>
<span data-ttu-id="9b8ef-120">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-120">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b8ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b8ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b8ef-122">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="9b8ef-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b8ef-123">-Confirm</span></span>
<span data-ttu-id="9b8ef-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b8ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b8ef-125">-WhatIf</span></span>
<span data-ttu-id="9b8ef-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b8ef-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b8ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8ef-128">CommonParameters</span></span>
<span data-ttu-id="9b8ef-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8ef-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b8ef-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8ef-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b8ef-131">INPUTS</span></span>

### <span data-ttu-id="9b8ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9b8ef-132">System.String</span></span>

### <span data-ttu-id="9b8ef-133">Microsoft. Azure. Management. Cognitivaservices. Models. KeyName</span><span class="sxs-lookup"><span data-stu-id="9b8ef-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="9b8ef-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b8ef-134">OUTPUTS</span></span>

### <span data-ttu-id="9b8ef-135">Microsoft. Azure. Management. Cognitivaservices. Models. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9b8ef-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="9b8ef-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b8ef-136">NOTES</span></span>

## <span data-ttu-id="9b8ef-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b8ef-137">RELATED LINKS</span></span>

[<span data-ttu-id="9b8ef-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b8ef-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


