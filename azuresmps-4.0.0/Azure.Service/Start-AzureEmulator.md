---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946031"
---
# <span data-ttu-id="fe1b7-101">Start-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="fe1b7-101">Start-AzureEmulator</span></span>

## <span data-ttu-id="fe1b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe1b7-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1b7-103">Inicia os emuladores de computação e armazenamento.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-103">Starts the compute and storage emulators.</span></span>

## <span data-ttu-id="fe1b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe1b7-104">SYNTAX</span></span>

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fe1b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe1b7-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1b7-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fe1b7-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="fe1b7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fe1b7-108">O cmdlet **Start-AzureEmulator** inicia o Compute e emuladores de armazenamento e hospeda o serviço atual no emulador de computação.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-108">The **Start-AzureEmulator** cmdlet starts both the compute and storage emulators and hosts the current service in the compute emulator.</span></span>

## <span data-ttu-id="fe1b7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe1b7-109">EXAMPLES</span></span>

### <span data-ttu-id="fe1b7-110">Exemplo 1: iniciar o emulador e iniciar um navegador</span><span class="sxs-lookup"><span data-stu-id="fe1b7-110">Example 1: Start the emulator and launch a browser</span></span>
```
PS C:\> Start-AzureEmulator -L
```

<span data-ttu-id="fe1b7-111">Este exemplo executa o serviço no emulador do Azure e abre uma nova janela do navegador no serviço emulado.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-111">This example runs the service in the Azure emulator and launches a new browser window on the emulated service.</span></span>

## <span data-ttu-id="fe1b7-112">OS</span><span class="sxs-lookup"><span data-stu-id="fe1b7-112">PARAMETERS</span></span>

### <span data-ttu-id="fe1b7-113">-Iniciar</span><span class="sxs-lookup"><span data-stu-id="fe1b7-113">-Launch</span></span>
<span data-ttu-id="fe1b7-114">Abre uma nova janela do navegador no serviço depois de hospeda-la no emulador.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-114">Opens a new browser window on the service after hosting it in the emulator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1b7-115">-Mode</span><span class="sxs-lookup"><span data-stu-id="fe1b7-115">-Mode</span></span>
<span data-ttu-id="fe1b7-116">Especifica o modo de emulador.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-116">Specifies the emulator mode.</span></span>
<span data-ttu-id="fe1b7-117">Os valores válidos são: completo e expresso.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-117">Valid values are: Full and Express.</span></span>
<span data-ttu-id="fe1b7-118">O valor padrão é Express.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-118">The default value is Express.</span></span>

```yaml
Type: ComputeEmulatorMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1b7-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fe1b7-119">-Profile</span></span>
<span data-ttu-id="fe1b7-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe1b7-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fe1b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1b7-122">CommonParameters</span></span>
<span data-ttu-id="fe1b7-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe1b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1b7-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1b7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1b7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe1b7-125">INPUTS</span></span>

## <span data-ttu-id="fe1b7-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe1b7-126">OUTPUTS</span></span>

## <span data-ttu-id="fe1b7-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe1b7-127">NOTES</span></span>

## <span data-ttu-id="fe1b7-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe1b7-128">RELATED LINKS</span></span>

[<span data-ttu-id="fe1b7-129">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="fe1b7-129">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="fe1b7-130">Publicar-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="fe1b7-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="fe1b7-131">Parar-AzureEmulator</span><span class="sxs-lookup"><span data-stu-id="fe1b7-131">Stop-AzureEmulator</span></span>](./Stop-AzureEmulator.md)


