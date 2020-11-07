---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 43E2C42E-16A3-426E-A7C4-33942F06F908
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd94462eb89cff6b4cec97f05911e27dbb05c920
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945766"
---
# <span data-ttu-id="52947-101">Stop-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="52947-101">Stop-AzureEmulator</span></span>

## <span data-ttu-id="52947-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="52947-102">SYNOPSIS</span></span>
<span data-ttu-id="52947-103">Interrompe o emulador de computação.</span><span class="sxs-lookup"><span data-stu-id="52947-103">Stops the compute emulator.</span></span>

## <span data-ttu-id="52947-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="52947-104">SYNTAX</span></span>

```
Stop-AzureEmulator [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="52947-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="52947-105">DESCRIPTION</span></span>
<span data-ttu-id="52947-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="52947-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="52947-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="52947-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="52947-108">O cmdlet **Stop-AzureEmulator** interrompe o emulador de computação do Azure.</span><span class="sxs-lookup"><span data-stu-id="52947-108">The **Stop-AzureEmulator** cmdlet stops the Azure compute emulator.</span></span>
<span data-ttu-id="52947-109">Qualquer serviço atualmente em execução no emulador será removido.</span><span class="sxs-lookup"><span data-stu-id="52947-109">Any services currently running in the emulator are removed.</span></span>

## <span data-ttu-id="52947-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="52947-110">EXAMPLES</span></span>

## <span data-ttu-id="52947-111">OS</span><span class="sxs-lookup"><span data-stu-id="52947-111">PARAMETERS</span></span>

### <span data-ttu-id="52947-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52947-112">-PassThru</span></span>
<span data-ttu-id="52947-113">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="52947-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52947-114">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="52947-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52947-115">-Perfil</span><span class="sxs-lookup"><span data-stu-id="52947-115">-Profile</span></span>
<span data-ttu-id="52947-116">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="52947-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="52947-117">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="52947-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="52947-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52947-118">CommonParameters</span></span>
<span data-ttu-id="52947-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52947-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52947-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52947-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52947-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="52947-121">INPUTS</span></span>

## <span data-ttu-id="52947-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="52947-122">OUTPUTS</span></span>

## <span data-ttu-id="52947-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="52947-123">NOTES</span></span>

## <span data-ttu-id="52947-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="52947-124">RELATED LINKS</span></span>

[<span data-ttu-id="52947-125">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="52947-125">Start-AzureEmulator</span></span>](./Start-AzureEmulator.md)


