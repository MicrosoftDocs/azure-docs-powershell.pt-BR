---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426587"
---
# <span data-ttu-id="d75c4-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="d75c4-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="d75c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d75c4-102">SYNOPSIS</span></span>
<span data-ttu-id="d75c4-103">Modifica o proprietário de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d75c4-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d75c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d75c4-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d75c4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d75c4-105">DESCRIPTION</span></span>
<span data-ttu-id="d75c4-106">O cmdlet **set-AzDataLakeStoreItemOwner** modifica o proprietário de um arquivo ou pasta no repositório data Lake.</span><span class="sxs-lookup"><span data-stu-id="d75c4-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d75c4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d75c4-107">EXAMPLES</span></span>

### <span data-ttu-id="d75c4-108">Exemplo 1: definir o proprietário de um item</span><span class="sxs-lookup"><span data-stu-id="d75c4-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="d75c4-109">Esse comando define o proprietário do diretório raiz como Patti a Pereira.</span><span class="sxs-lookup"><span data-stu-id="d75c4-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="d75c4-110">OS</span><span class="sxs-lookup"><span data-stu-id="d75c4-110">PARAMETERS</span></span>

### <span data-ttu-id="d75c4-111">-Conta</span><span class="sxs-lookup"><span data-stu-id="d75c4-111">-Account</span></span>
<span data-ttu-id="d75c4-112">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d75c4-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75c4-113">-DefaultProfile</span></span>
<span data-ttu-id="d75c4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d75c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d75c4-115">-ID</span><span class="sxs-lookup"><span data-stu-id="d75c4-115">-Id</span></span>
<span data-ttu-id="d75c4-116">Especifica a ID de objeto do usuário, grupo ou entidade de serviço do diretório do AzureActive a ser usado como proprietário.</span><span class="sxs-lookup"><span data-stu-id="d75c4-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75c4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d75c4-117">-PassThru</span></span>
<span data-ttu-id="d75c4-118">Indica que o proprietário atualizado resultante deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="d75c4-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="d75c4-119">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d75c4-119">-Path</span></span>
<span data-ttu-id="d75c4-120">Especifica o caminho do repositório data Lake do item a ser modificado, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="d75c4-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75c4-121">-Digite</span><span class="sxs-lookup"><span data-stu-id="d75c4-121">-Type</span></span>
<span data-ttu-id="d75c4-122">Especifica o tipo de proprietário a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d75c4-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="d75c4-123">Os valores aceitáveis para esse parâmetro são: usuário e grupo.</span><span class="sxs-lookup"><span data-stu-id="d75c4-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75c4-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d75c4-124">-Confirm</span></span>
<span data-ttu-id="d75c4-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75c4-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75c4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d75c4-126">-WhatIf</span></span>
<span data-ttu-id="d75c4-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d75c4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d75c4-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d75c4-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75c4-129">CommonParameters</span></span>
<span data-ttu-id="d75c4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75c4-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d75c4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75c4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d75c4-132">INPUTS</span></span>

### <span data-ttu-id="d75c4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d75c4-133">System.String</span></span>

### <span data-ttu-id="d75c4-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d75c4-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d75c4-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="d75c4-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="d75c4-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d75c4-136">System.Guid</span></span>

### <span data-ttu-id="d75c4-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d75c4-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d75c4-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d75c4-138">OUTPUTS</span></span>

### <span data-ttu-id="d75c4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d75c4-139">System.String</span></span>

## <span data-ttu-id="d75c4-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d75c4-140">NOTES</span></span>

## <span data-ttu-id="d75c4-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d75c4-141">RELATED LINKS</span></span>

[<span data-ttu-id="d75c4-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="d75c4-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


