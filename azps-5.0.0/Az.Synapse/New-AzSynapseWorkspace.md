---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125233"
---
# <span data-ttu-id="2f9af-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2f9af-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="2f9af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f9af-102">SYNOPSIS</span></span>
<span data-ttu-id="2f9af-103">Cria um espaço de trabalho de análise do Synapse.</span><span class="sxs-lookup"><span data-stu-id="2f9af-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2f9af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f9af-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f9af-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f9af-105">DESCRIPTION</span></span>
<span data-ttu-id="2f9af-106">O cmdlet **New-AzSynapseWorkspace** cria um espaço de trabalho de análise do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="2f9af-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="2f9af-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f9af-107">EXAMPLES</span></span>

### <span data-ttu-id="2f9af-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2f9af-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="2f9af-109">Esse comando cria um espaço de trabalho de análise Synapse chamado ContosoWorkspace que usa o repositório de dados ContosoAdlGenStorage, no grupo de recursos chamado ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2f9af-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="2f9af-110">OS</span><span class="sxs-lookup"><span data-stu-id="2f9af-110">PARAMETERS</span></span>

### <span data-ttu-id="2f9af-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f9af-111">-AsJob</span></span>
<span data-ttu-id="2f9af-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2f9af-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f9af-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2f9af-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="2f9af-114">O nome da conta de armazenamento ADLS Gen2 padrão.</span><span class="sxs-lookup"><span data-stu-id="2f9af-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="2f9af-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="2f9af-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="2f9af-116">O sistema de arquivos ADLS Gen2 padrão.</span><span class="sxs-lookup"><span data-stu-id="2f9af-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="2f9af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f9af-117">-DefaultProfile</span></span>
<span data-ttu-id="2f9af-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f9af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f9af-119">-Local</span><span class="sxs-lookup"><span data-stu-id="2f9af-119">-Location</span></span>
<span data-ttu-id="2f9af-120">Região do Azure na qual o recurso deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="2f9af-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="2f9af-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2f9af-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="2f9af-122">Nome de uma rede virtual gerenciada pela Synapse dedicada para o espaço de trabalho do Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="2f9af-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f9af-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f9af-123">-Name</span></span>
<span data-ttu-id="2f9af-124">Nome do espaço de trabalho do Synapse.</span><span class="sxs-lookup"><span data-stu-id="2f9af-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f9af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f9af-125">-ResourceGroupName</span></span>
<span data-ttu-id="2f9af-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f9af-126">Resource group name.</span></span>

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

### <span data-ttu-id="2f9af-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="2f9af-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="2f9af-128">Credenciais de administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="2f9af-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f9af-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="2f9af-129">-Tag</span></span>
<span data-ttu-id="2f9af-130">Uma cadeia de caracteres, dicionário de cadeias de caracteres de marcas associadas ao recurso.</span><span class="sxs-lookup"><span data-stu-id="2f9af-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f9af-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2f9af-131">-Confirm</span></span>
<span data-ttu-id="2f9af-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f9af-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f9af-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f9af-133">-WhatIf</span></span>
<span data-ttu-id="2f9af-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f9af-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f9af-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f9af-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f9af-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f9af-136">CommonParameters</span></span>
<span data-ttu-id="2f9af-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f9af-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f9af-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f9af-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f9af-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f9af-139">INPUTS</span></span>

### <span data-ttu-id="2f9af-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2f9af-140">System.String</span></span>

### <span data-ttu-id="2f9af-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2f9af-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2f9af-142">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="2f9af-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="2f9af-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f9af-143">OUTPUTS</span></span>

### <span data-ttu-id="2f9af-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2f9af-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="2f9af-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f9af-145">NOTES</span></span>

## <span data-ttu-id="2f9af-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f9af-146">RELATED LINKS</span></span>
