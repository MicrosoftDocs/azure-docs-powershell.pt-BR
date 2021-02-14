---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D53DAEB6-DC4F-473C-A193-A1E2A65326D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplicationPackage.md
ms.openlocfilehash: fc23c99cabe76834204f2fac1f3c18ae7eea1df0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115984"
---
# <span data-ttu-id="8c3e8-101">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8c3e8-101">New-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="8c3e8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8c3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3e8-103">Cria um pacote de aplicativos em uma conta em lote.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-103">Creates an application package in a Batch account.</span></span>

## <span data-ttu-id="8c3e8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c3e8-104">SYNTAX</span></span>

### <span data-ttu-id="8c3e8-105">UploadAndActivate (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8c3e8-105">UploadAndActivate (Default)</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> -FilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c3e8-106">ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="8c3e8-106">ActivateOnly</span></span>
```
New-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-ApplicationVersion] <String> [-Format] <String> [-ActivateOnly] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c3e8-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c3e8-107">DESCRIPTION</span></span>
<span data-ttu-id="8c3e8-108">O cmdlet **New-AzBatchApplicationPackage** cria um pacote de aplicativos em uma conta do Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-108">The **New-AzBatchApplicationPackage** cmdlet creates an application package in an Azure Batch account.</span></span>

## <span data-ttu-id="8c3e8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c3e8-109">EXAMPLES</span></span>

### <span data-ttu-id="8c3e8-110">Exemplo 1: Instalar um pacote de aplicativos em uma conta em lote</span><span class="sxs-lookup"><span data-stu-id="8c3e8-110">Example 1: Install an application package into a Batch account</span></span>
```
PS C:\>New-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -ApplicationVersion "1.0" -FilePath "litware.1.0.zip" -Format "zip"
```

<span data-ttu-id="8c3e8-111">Esse comando cria e ativa a versão 1.0 do aplicativo Litware e carrega o conteúdo do litware.1.0.zip como conteúdo do pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-111">This command creates and activates version 1.0 of the Litware application, and uploads the contents of litware.1.0.zip as the application package content.</span></span>

## <span data-ttu-id="8c3e8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c3e8-112">PARAMETERS</span></span>

### <span data-ttu-id="8c3e8-113">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="8c3e8-113">-AccountName</span></span>
<span data-ttu-id="8c3e8-114">Especifica o nome da conta Em lotes à qual este cmdlet adiciona um pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-114">Specifies the name of the Batch account to which this cmdlet adds an application package.</span></span>

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

### <span data-ttu-id="8c3e8-115">-ActivateOnly</span><span class="sxs-lookup"><span data-stu-id="8c3e8-115">-ActivateOnly</span></span>
<span data-ttu-id="8c3e8-116">Indica que esse cmdlet ativa um pacote de aplicativos que já foi carregado.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-116">Indicates that this cmdlet activates an application package that has already been uploaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ActivateOnly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3e8-117">-Nomedo Aplicativo</span><span class="sxs-lookup"><span data-stu-id="8c3e8-117">-ApplicationName</span></span>
<span data-ttu-id="8c3e8-118">Especifica o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-118">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3e8-119">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="8c3e8-119">-ApplicationVersion</span></span>
<span data-ttu-id="8c3e8-120">Especifica a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-120">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3e8-121">-DefaultProfile</span></span>
<span data-ttu-id="8c3e8-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c3e8-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="8c3e8-123">-FilePath</span></span>
<span data-ttu-id="8c3e8-124">Especifica o arquivo a ser carregado como o arquivo binário do pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-124">Specifies the file to be uploaded as the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadAndActivate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3e8-125">-Formatar</span><span class="sxs-lookup"><span data-stu-id="8c3e8-125">-Format</span></span>
<span data-ttu-id="8c3e8-126">Especifica o formato do arquivo binário do pacote de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-126">Specifies the format of the application package binary file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c3e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c3e8-128">Especifica o nome do grupo de recursos que contém a conta Lote.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-128">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="8c3e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3e8-129">CommonParameters</span></span>
<span data-ttu-id="8c3e8-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c3e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3e8-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c3e8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3e8-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="8c3e8-132">INPUTS</span></span>

### <span data-ttu-id="8c3e8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8c3e8-133">System.String</span></span>

### <span data-ttu-id="8c3e8-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8c3e8-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8c3e8-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="8c3e8-135">OUTPUTS</span></span>

### <span data-ttu-id="8c3e8-136">Microsoft.Azure.Commands.Batch. Models.PSApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8c3e8-136">Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage</span></span>

## <span data-ttu-id="8c3e8-137">Notas</span><span class="sxs-lookup"><span data-stu-id="8c3e8-137">NOTES</span></span>

## <span data-ttu-id="8c3e8-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8c3e8-138">RELATED LINKS</span></span>

[<span data-ttu-id="8c3e8-139">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8c3e8-139">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="8c3e8-140">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8c3e8-140">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="8c3e8-141">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8c3e8-141">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="8c3e8-142">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8c3e8-142">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="8c3e8-143">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="8c3e8-143">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="8c3e8-144">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="8c3e8-144">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


