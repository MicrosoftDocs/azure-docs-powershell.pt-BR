---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 03107EA1-6ADA-4A3E-B8E1-88788E5F3F37
online version: ''
schema: 2.0.0
ms.openlocfilehash: 21892d129319977897a6855933e3e8542460a4a4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946127"
---
# <span data-ttu-id="d3f7a-101">Remove-AzureService</span><span class="sxs-lookup"><span data-stu-id="d3f7a-101">Remove-AzureService</span></span>

## <span data-ttu-id="d3f7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f7a-103">Remove o serviço de nuvem atual.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-103">Removes the current cloud service.</span></span>

## <span data-ttu-id="d3f7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3f7a-104">SYNTAX</span></span>

```
Remove-AzureService [-ServiceName <String>] [-Force] [-PassThru] [-DeleteAll] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f7a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3f7a-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f7a-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d3f7a-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="d3f7a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="d3f7a-108">O cmdlet **Remove-AzureService** interrompe e remove o serviço de nuvem atual ou o serviço que corresponde ao serviço e ao nome de assinatura especificados.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-108">The **Remove-AzureService** cmdlet stops and removes the current cloud service, or the service matching the specified service and subscription name.</span></span>

## <span data-ttu-id="d3f7a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3f7a-109">EXAMPLES</span></span>

## <span data-ttu-id="d3f7a-110">OS</span><span class="sxs-lookup"><span data-stu-id="d3f7a-110">PARAMETERS</span></span>

### <span data-ttu-id="d3f7a-111">-DeleteAll</span><span class="sxs-lookup"><span data-stu-id="d3f7a-111">-DeleteAll</span></span>
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

### <span data-ttu-id="d3f7a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="d3f7a-112">-Force</span></span>
<span data-ttu-id="d3f7a-113">Remove o serviço sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-113">Removes the service without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d3f7a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3f7a-114">-PassThru</span></span>
<span data-ttu-id="d3f7a-115">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3f7a-116">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3f7a-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d3f7a-117">-Profile</span></span>
<span data-ttu-id="d3f7a-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3f7a-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f7a-120">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d3f7a-120">-ServiceName</span></span>
<span data-ttu-id="d3f7a-121">Especifica o nome do serviço a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-121">Specifies the name of the service to be removed.</span></span>
<span data-ttu-id="d3f7a-122">Se o comando for executado de um diretório de serviço e nenhum nome for especificado, usará o nome do serviço atual.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-122">If the command is run from a service directory and no name is specified, uses the current service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f7a-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3f7a-123">-Confirm</span></span>
<span data-ttu-id="d3f7a-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f7a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f7a-125">-WhatIf</span></span>
<span data-ttu-id="d3f7a-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f7a-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f7a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f7a-128">CommonParameters</span></span>
<span data-ttu-id="d3f7a-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f7a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f7a-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f7a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f7a-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3f7a-131">INPUTS</span></span>

## <span data-ttu-id="d3f7a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3f7a-132">OUTPUTS</span></span>

## <span data-ttu-id="d3f7a-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3f7a-133">NOTES</span></span>

## <span data-ttu-id="d3f7a-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3f7a-134">RELATED LINKS</span></span>

[<span data-ttu-id="d3f7a-135">Publicar-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="d3f7a-135">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="d3f7a-136">Parar-AzureService</span><span class="sxs-lookup"><span data-stu-id="d3f7a-136">Stop-AzureService</span></span>](./Stop-AzureService.md)

[<span data-ttu-id="d3f7a-137">Start-AzureService</span><span class="sxs-lookup"><span data-stu-id="d3f7a-137">Start-AzureService</span></span>](./Start-AzureService.md)


