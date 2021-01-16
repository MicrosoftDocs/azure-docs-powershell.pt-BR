---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428448"
---
# <span data-ttu-id="22d26-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22d26-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="22d26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22d26-102">SYNOPSIS</span></span>
<span data-ttu-id="22d26-103">Cria uma nova conta de armazenamento de borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="22d26-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="22d26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22d26-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22d26-105">DESCRIPTION</span></span>
<span data-ttu-id="22d26-106">O cmdlet **New-AzStackEdgeStorageAccount** cria uma nova conta de armazenamento de borda em um dispositivo de borda de pilha.</span><span class="sxs-lookup"><span data-stu-id="22d26-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="22d26-107">Para um dispositivo, uma conta de armazenamento de borda pode ser mapeada no máximo para apenas uma conta de armazenamento em nuvem.</span><span class="sxs-lookup"><span data-stu-id="22d26-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="22d26-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22d26-108">EXAMPLES</span></span>

### <span data-ttu-id="22d26-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22d26-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="22d26-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="22d26-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="22d26-111">2 EdgeStorageAccounts no dispositivo não pode compartilhar mais do que uma conta de armazenamento em nuvem</span><span class="sxs-lookup"><span data-stu-id="22d26-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="22d26-112">OS</span><span class="sxs-lookup"><span data-stu-id="22d26-112">PARAMETERS</span></span>

### <span data-ttu-id="22d26-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22d26-113">-AsJob</span></span>
<span data-ttu-id="22d26-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="22d26-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22d26-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="22d26-115">-Cloud</span></span>
<span data-ttu-id="22d26-116">Usará um CloudStorageAccount para hierarquização</span><span class="sxs-lookup"><span data-stu-id="22d26-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d26-117">-DefaultProfile</span></span>
<span data-ttu-id="22d26-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22d26-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d26-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="22d26-119">-DeviceName</span></span>
<span data-ttu-id="22d26-120">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="22d26-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22d26-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="22d26-121">-Name</span></span>
<span data-ttu-id="22d26-122">Nome do recurso</span><span class="sxs-lookup"><span data-stu-id="22d26-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeStorageAccount

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22d26-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d26-123">-ResourceGroupName</span></span>
<span data-ttu-id="22d26-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="22d26-124">Resource Group Name</span></span>

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

### <span data-ttu-id="22d26-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="22d26-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="22d26-126">Fornecer o nome do recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="22d26-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="22d26-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="22d26-127">-Confirm</span></span>
<span data-ttu-id="22d26-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22d26-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d26-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d26-129">-WhatIf</span></span>
<span data-ttu-id="22d26-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="22d26-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22d26-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="22d26-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d26-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d26-132">CommonParameters</span></span>
<span data-ttu-id="22d26-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d26-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d26-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22d26-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d26-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22d26-135">INPUTS</span></span>

### <span data-ttu-id="22d26-136">System. String</span><span class="sxs-lookup"><span data-stu-id="22d26-136">System.String</span></span>

### <span data-ttu-id="22d26-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="22d26-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="22d26-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22d26-138">OUTPUTS</span></span>

### <span data-ttu-id="22d26-139">Microsoft. Azure. PowerShell. cmdlets. StackEdge. Models. PSStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22d26-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="22d26-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22d26-140">NOTES</span></span>

## <span data-ttu-id="22d26-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22d26-141">RELATED LINKS</span></span>
