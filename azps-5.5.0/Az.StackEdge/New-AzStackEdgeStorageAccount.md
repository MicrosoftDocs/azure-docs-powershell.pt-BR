---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageAccount.md
ms.openlocfilehash: 815b8a7feb22e754302c455c7666f8408c348c92
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113683"
---
# <span data-ttu-id="45cd5-101">New-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45cd5-101">New-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="45cd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="45cd5-103">Cria uma nova conta de Armazenamento de Borda no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45cd5-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="45cd5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45cd5-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45cd5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="45cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="45cd5-106">O **cmdlet New-AzSt stackEdgeStorageAccount** cria uma nova conta de Armazenamento de Borda em um dispositivo stack edge.</span><span class="sxs-lookup"><span data-stu-id="45cd5-106">The **New-AzStackEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Stack Edge device.</span></span> <span data-ttu-id="45cd5-107">Para um dispositivo, uma conta de Armazenamento de Borda pode ser mapeada no máximo para apenas uma conta de Armazenamento em Nuvem.</span><span class="sxs-lookup"><span data-stu-id="45cd5-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="45cd5-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45cd5-108">EXAMPLES</span></span>

### <span data-ttu-id="45cd5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="45cd5-109">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="45cd5-110">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="45cd5-110">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="45cd5-111">2 EdgeStorageAccounts no dispositivo não pode compartilhar mais de 1 Conta de Armazenamento em Nuvem</span><span class="sxs-lookup"><span data-stu-id="45cd5-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="45cd5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45cd5-112">PARAMETERS</span></span>

### <span data-ttu-id="45cd5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45cd5-113">-AsJob</span></span>
<span data-ttu-id="45cd5-114">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="45cd5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45cd5-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="45cd5-115">-Cloud</span></span>
<span data-ttu-id="45cd5-116">Usará uma CloudStorageAccount para a classificação de camadas</span><span class="sxs-lookup"><span data-stu-id="45cd5-116">Will use a CloudStorageAccount for tiering</span></span>

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

### <span data-ttu-id="45cd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45cd5-117">-DefaultProfile</span></span>
<span data-ttu-id="45cd5-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45cd5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45cd5-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="45cd5-119">-DeviceName</span></span>
<span data-ttu-id="45cd5-120">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="45cd5-120">Device Name</span></span>

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

### <span data-ttu-id="45cd5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="45cd5-121">-Name</span></span>
<span data-ttu-id="45cd5-122">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="45cd5-122">Resource Name</span></span>

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

### <span data-ttu-id="45cd5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45cd5-123">-ResourceGroupName</span></span>
<span data-ttu-id="45cd5-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="45cd5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="45cd5-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="45cd5-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="45cd5-126">Fornecer o Nome de Recurso de StorageAccountCredential existente</span><span class="sxs-lookup"><span data-stu-id="45cd5-126">Provide existing StorageAccountCredential's Resource Name</span></span>

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

### <span data-ttu-id="45cd5-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="45cd5-127">-Confirm</span></span>
<span data-ttu-id="45cd5-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45cd5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45cd5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45cd5-129">-WhatIf</span></span>
<span data-ttu-id="45cd5-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="45cd5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45cd5-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45cd5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45cd5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45cd5-132">CommonParameters</span></span>
<span data-ttu-id="45cd5-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45cd5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45cd5-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45cd5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45cd5-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="45cd5-135">INPUTS</span></span>

### <span data-ttu-id="45cd5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="45cd5-136">System.String</span></span>

### <span data-ttu-id="45cd5-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="45cd5-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="45cd5-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="45cd5-138">OUTPUTS</span></span>

### <span data-ttu-id="45cd5-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="45cd5-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="45cd5-140">Notas</span><span class="sxs-lookup"><span data-stu-id="45cd5-140">NOTES</span></span>

## <span data-ttu-id="45cd5-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45cd5-141">RELATED LINKS</span></span>
