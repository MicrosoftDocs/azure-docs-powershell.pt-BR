---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 501a164fc4470a3d4fd6163050fba495ce3d2705
ms.sourcegitcommit: 25eca7b5f5480758aa2cd830458900cf91cf673c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/24/2020
ms.locfileid: "95515084"
---
# <span data-ttu-id="28285-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="28285-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="28285-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28285-102">SYNOPSIS</span></span>
<span data-ttu-id="28285-103">Interrompe o emulador de computação.</span><span class="sxs-lookup"><span data-stu-id="28285-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="28285-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28285-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="28285-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28285-105">DESCRIPTION</span></span>
<span data-ttu-id="28285-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="28285-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="28285-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="28285-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="28285-108">O cmdlet **Stop-AzureEmulator** interrompe o emulador de computação do Azure.</span><span class="sxs-lookup"><span data-stu-id="28285-108">The **Stop-AzureEmulator** cmdlet stops the Azure Compute Emulator.</span></span>
<span data-ttu-id="28285-109">Qualquer serviço atualmente em execução no emulador será removido.</span><span class="sxs-lookup"><span data-stu-id="28285-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="28285-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28285-110">EXAMPLES</span></span>

## <span data-ttu-id="28285-111">OS</span><span class="sxs-lookup"><span data-stu-id="28285-111">PARAMETERS</span></span>

### <span data-ttu-id="28285-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28285-112">-PassThru</span></span>
<span data-ttu-id="28285-113">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="28285-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28285-114">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="28285-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28285-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="28285-115">-Profile</span></span>
<span data-ttu-id="28285-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="28285-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28285-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="28285-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28285-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28285-118">CommonParameters</span></span>
<span data-ttu-id="28285-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28285-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28285-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28285-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28285-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28285-121">INPUTS</span></span>

## <span data-ttu-id="28285-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28285-122">OUTPUTS</span></span>

## <span data-ttu-id="28285-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28285-123">NOTES</span></span>

## <span data-ttu-id="28285-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28285-124">RELATED LINKS</span></span>

[<span data-ttu-id="28285-125">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="28285-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


