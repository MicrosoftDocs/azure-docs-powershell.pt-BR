---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433983"
---
# <span data-ttu-id="96f69-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="96f69-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="96f69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="96f69-102">SYNOPSIS</span></span>
<span data-ttu-id="96f69-103">Obtém as credenciais de databox de um trabalho específico</span><span class="sxs-lookup"><span data-stu-id="96f69-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="96f69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="96f69-104">SYNTAX</span></span>

### <span data-ttu-id="96f69-105">GetByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="96f69-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96f69-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="96f69-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96f69-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="96f69-107">DESCRIPTION</span></span>
<span data-ttu-id="96f69-108">O cmdlet **Get-AzDataBoxCredential** Obtém as credenciais do databox de um trabalho específico.</span><span class="sxs-lookup"><span data-stu-id="96f69-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="96f69-109">As propriedades internas do objeto de credenciais retornado serão diferentes para tipos de SKU diferentes.</span><span class="sxs-lookup"><span data-stu-id="96f69-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="96f69-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="96f69-110">EXAMPLES</span></span>

### <span data-ttu-id="96f69-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="96f69-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="96f69-112">Isso retuns o JobSecrets do trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="96f69-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="96f69-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="96f69-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="96f69-114">Isso retuns o JobSecrets do trabalho especificado</span><span class="sxs-lookup"><span data-stu-id="96f69-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="96f69-115">OS</span><span class="sxs-lookup"><span data-stu-id="96f69-115">PARAMETERS</span></span>

### <span data-ttu-id="96f69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96f69-116">-DefaultProfile</span></span>
<span data-ttu-id="96f69-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="96f69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96f69-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="96f69-118">-Name</span></span>
<span data-ttu-id="96f69-119">Nome do trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="96f69-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f69-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96f69-120">-ResourceGroupName</span></span>
<span data-ttu-id="96f69-121">Nome do grupo de recursos de trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="96f69-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96f69-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96f69-122">-ResourceId</span></span>
<span data-ttu-id="96f69-123">ID do recurso do trabalho Databox</span><span class="sxs-lookup"><span data-stu-id="96f69-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96f69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96f69-124">CommonParameters</span></span>
<span data-ttu-id="96f69-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96f69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96f69-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96f69-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96f69-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="96f69-127">INPUTS</span></span>

### <span data-ttu-id="96f69-128">System. String</span><span class="sxs-lookup"><span data-stu-id="96f69-128">System.String</span></span>

## <span data-ttu-id="96f69-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="96f69-129">OUTPUTS</span></span>

### <span data-ttu-id="96f69-130">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Management. DataBox. Models. UnencryptedCredentials, Microsoft. Azure. Management. DataBox, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="96f69-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="96f69-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="96f69-131">NOTES</span></span>

## <span data-ttu-id="96f69-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="96f69-132">RELATED LINKS</span></span>
