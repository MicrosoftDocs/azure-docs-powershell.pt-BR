---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946012"
---
# <span data-ttu-id="a0f81-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="a0f81-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="a0f81-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0f81-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f81-103">Interrompe um trabalho do StorSimple.</span><span class="sxs-lookup"><span data-stu-id="a0f81-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="a0f81-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0f81-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a0f81-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0f81-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f81-106">O cmdlet **Stop-AzureStorSimpleJob** interrompe um trabalho do StorSimple em andamento.</span><span class="sxs-lookup"><span data-stu-id="a0f81-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="a0f81-107">Você pode especificar um trabalho fornecendo uma ID de instância ou um nome de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a0f81-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="a0f81-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0f81-108">EXAMPLES</span></span>

### <span data-ttu-id="a0f81-109">Exemplo 1: interromper trabalhos para um dispositivo</span><span class="sxs-lookup"><span data-stu-id="a0f81-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="a0f81-110">Esse comando obtém os trabalhos para o dispositivo chamado Device07, usando o cmdlet **Get-AzureStorSimpleJob** .</span><span class="sxs-lookup"><span data-stu-id="a0f81-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="a0f81-111">O comando passa os trabalhos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="a0f81-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a0f81-112">O cmdlet atual interrompe qualquer trabalho que o comando passa para ele.</span><span class="sxs-lookup"><span data-stu-id="a0f81-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="a0f81-113">O comando especifica o parâmetro *Force* e, portanto, não solicita confirmação antes de parar um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a0f81-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="a0f81-114">Exemplo 2: parar um trabalho específico</span><span class="sxs-lookup"><span data-stu-id="a0f81-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="a0f81-115">Esse comando interrompe o trabalho que tem a ID de instância especificada.</span><span class="sxs-lookup"><span data-stu-id="a0f81-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="a0f81-116">OS</span><span class="sxs-lookup"><span data-stu-id="a0f81-116">PARAMETERS</span></span>

### <span data-ttu-id="a0f81-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a0f81-117">-Force</span></span>
<span data-ttu-id="a0f81-118">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a0f81-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0f81-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a0f81-119">-InstanceId</span></span>
<span data-ttu-id="a0f81-120">Especifica a ID do trabalho do dispositivo para parar.</span><span class="sxs-lookup"><span data-stu-id="a0f81-120">Specifies the ID of the device job to stop.</span></span>

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

### <span data-ttu-id="a0f81-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="a0f81-121">-Profile</span></span>
<span data-ttu-id="a0f81-122">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0f81-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a0f81-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f81-123">CommonParameters</span></span>
<span data-ttu-id="a0f81-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f81-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f81-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f81-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f81-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0f81-126">INPUTS</span></span>

### <span data-ttu-id="a0f81-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a0f81-127">None</span></span>

## <span data-ttu-id="a0f81-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0f81-128">OUTPUTS</span></span>

### <span data-ttu-id="a0f81-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="a0f81-129">DeviceJobDetails</span></span>
<span data-ttu-id="a0f81-130">Esse cmdlet obtém detalhes do **DeviceJob** que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="a0f81-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="a0f81-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0f81-131">NOTES</span></span>

## <span data-ttu-id="a0f81-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0f81-132">RELATED LINKS</span></span>

[<span data-ttu-id="a0f81-133">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="a0f81-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


