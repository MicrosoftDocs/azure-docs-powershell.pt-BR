---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777146"
---
# <span data-ttu-id="85b49-101">Stop-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="85b49-101">Stop-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="85b49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85b49-102">SYNOPSIS</span></span>
<span data-ttu-id="85b49-103">Cancelar um trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="85b49-103">Cancel a disk migration job.</span></span>

## <span data-ttu-id="85b49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85b49-104">SYNTAX</span></span>

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85b49-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85b49-105">DESCRIPTION</span></span>
<span data-ttu-id="85b49-106">Cancelar um trabalho de migração de disco.</span><span class="sxs-lookup"><span data-stu-id="85b49-106">Cancel a disk migration job.</span></span>

## <span data-ttu-id="85b49-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85b49-107">EXAMPLES</span></span>

### <span data-ttu-id="85b49-108">Exemplo 1:</span><span class="sxs-lookup"><span data-stu-id="85b49-108">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="85b49-109">Cancelar um trabalho de migração de disco gerenciado.</span><span class="sxs-lookup"><span data-stu-id="85b49-109">Cancel a managed disk migration job.</span></span>

## <span data-ttu-id="85b49-110">OS</span><span class="sxs-lookup"><span data-stu-id="85b49-110">PARAMETERS</span></span>

### <span data-ttu-id="85b49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b49-111">-DefaultProfile</span></span>
<span data-ttu-id="85b49-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85b49-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85b49-113">-Local</span><span class="sxs-lookup"><span data-stu-id="85b49-113">-Location</span></span>
<span data-ttu-id="85b49-114">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="85b49-114">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85b49-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="85b49-115">-Name</span></span>
<span data-ttu-id="85b49-116">O nome do GUID do trabalho de migração.</span><span class="sxs-lookup"><span data-stu-id="85b49-116">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85b49-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="85b49-117">-SubscriptionId</span></span>
<span data-ttu-id="85b49-118">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="85b49-118">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="85b49-119">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="85b49-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85b49-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85b49-120">-Confirm</span></span>
<span data-ttu-id="85b49-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85b49-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85b49-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85b49-122">-WhatIf</span></span>
<span data-ttu-id="85b49-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85b49-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85b49-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85b49-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85b49-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b49-125">CommonParameters</span></span>
<span data-ttu-id="85b49-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b49-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b49-127">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85b49-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b49-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85b49-128">INPUTS</span></span>

## <span data-ttu-id="85b49-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85b49-129">OUTPUTS</span></span>

### <span data-ttu-id="85b49-130">Microsoft. Azure. PowerShell. cmdlets. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="85b49-130">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="85b49-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85b49-131">NOTES</span></span>

## <span data-ttu-id="85b49-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85b49-132">RELATED LINKS</span></span>

