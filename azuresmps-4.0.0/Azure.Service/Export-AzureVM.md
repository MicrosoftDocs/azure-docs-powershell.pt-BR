---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 78099E89-63C9-4019-A4ED-EF37D2383A09
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23e6165e50c227320875fa70e97d63b0cdd78781
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945677"
---
# <span data-ttu-id="3da9c-101">Export-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3da9c-101">Export-AzureVM</span></span>

## <span data-ttu-id="3da9c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3da9c-102">SYNOPSIS</span></span>
<span data-ttu-id="3da9c-103">Exporta um estado da máquina virtual do Azure para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="3da9c-103">Exports an Azure virtual machine state to a file.</span></span>

## <span data-ttu-id="3da9c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3da9c-104">SYNTAX</span></span>

```
Export-AzureVM [-ServiceName] <String> [-Name] <String> [-Path] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3da9c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3da9c-105">DESCRIPTION</span></span>
<span data-ttu-id="3da9c-106">O cmdlet **Export-AzureVM** exporta o estado de uma máquina virtual para um arquivo. xml.</span><span class="sxs-lookup"><span data-stu-id="3da9c-106">The **Export-AzureVM** cmdlet exports the state of a virtual machine to an .xml file.</span></span>

<span data-ttu-id="3da9c-107">Executando **Export-AzureVM** , seguido de **Remove-AzureVM** e, em seguida, **Import-AzureVM** para recriar uma máquina virtual pode fazer com que a máquina virtual resultante tenha um endereço IP diferente do original.</span><span class="sxs-lookup"><span data-stu-id="3da9c-107">Running **Export-AzureVM** , followed by **Remove-AzureVM** and then **Import-AzureVM** to recreate a virtual machine can cause the resultant virtual machine to have a different IP address than the original.</span></span>

## <span data-ttu-id="3da9c-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3da9c-108">EXAMPLES</span></span>

### <span data-ttu-id="3da9c-109">Exemplo 1: exportar uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="3da9c-109">Example 1: Export a virtual machine</span></span>
```
PS C:\> Export-AzureVM -ServiceName "ContosoService" -Name "ContosoRole06" -Path "C:\vms\VMstate.xml"
```

<span data-ttu-id="3da9c-110">Esse comando exporta o estado da máquina virtual especificada para o arquivo VMstate.xml.</span><span class="sxs-lookup"><span data-stu-id="3da9c-110">This command exports the state of the specified virtual machine to the VMstate.xml file.</span></span>

## <span data-ttu-id="3da9c-111">OS</span><span class="sxs-lookup"><span data-stu-id="3da9c-111">PARAMETERS</span></span>

### <span data-ttu-id="3da9c-112">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="3da9c-112">-InformationAction</span></span>
<span data-ttu-id="3da9c-113">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="3da9c-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3da9c-114">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3da9c-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3da9c-115">Contínuo</span><span class="sxs-lookup"><span data-stu-id="3da9c-115">Continue</span></span>
- <span data-ttu-id="3da9c-116">Ignorar</span><span class="sxs-lookup"><span data-stu-id="3da9c-116">Ignore</span></span>
- <span data-ttu-id="3da9c-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="3da9c-117">Inquire</span></span>
- <span data-ttu-id="3da9c-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3da9c-118">SilentlyContinue</span></span>
- <span data-ttu-id="3da9c-119">Finaliza</span><span class="sxs-lookup"><span data-stu-id="3da9c-119">Stop</span></span>
- <span data-ttu-id="3da9c-120">Suspensão</span><span class="sxs-lookup"><span data-stu-id="3da9c-120">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3da9c-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3da9c-121">-InformationVariable</span></span>
<span data-ttu-id="3da9c-122">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="3da9c-122">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3da9c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3da9c-123">-Name</span></span>
<span data-ttu-id="3da9c-124">Especifica o nome da máquina virtual para a qual esse cmdlet exporta o estado.</span><span class="sxs-lookup"><span data-stu-id="3da9c-124">Specifies the name of the virtual machine for which this cmdlet exports state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da9c-125">-Caminho</span><span class="sxs-lookup"><span data-stu-id="3da9c-125">-Path</span></span>
<span data-ttu-id="3da9c-126">Especifica o caminho e o nome do arquivo para o qual esse cmdlet salva o estado da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3da9c-126">Specifies the path and file name to which this cmdlet saves the virtual machine state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3da9c-127">-Perfil</span><span class="sxs-lookup"><span data-stu-id="3da9c-127">-Profile</span></span>
<span data-ttu-id="3da9c-128">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="3da9c-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3da9c-129">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="3da9c-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3da9c-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3da9c-130">-ServiceName</span></span>
<span data-ttu-id="3da9c-131">Especifica o nome do serviço do Azure que hospeda a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3da9c-131">Specifies the name of the Azure service that hosts the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3da9c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da9c-132">CommonParameters</span></span>
<span data-ttu-id="3da9c-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3da9c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da9c-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da9c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da9c-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3da9c-135">INPUTS</span></span>

## <span data-ttu-id="3da9c-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3da9c-136">OUTPUTS</span></span>

## <span data-ttu-id="3da9c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3da9c-137">NOTES</span></span>

## <span data-ttu-id="3da9c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3da9c-138">RELATED LINKS</span></span>

[<span data-ttu-id="3da9c-139">Import-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3da9c-139">Import-AzureVM</span></span>](./Import-AzureVM.md)


