---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsqlserverextension
schema: 2.0.0
ms.openlocfilehash: aa37745469ad6610fa2511d49c3404bbf54d8059
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786152"
---
# <span data-ttu-id="06fab-101">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="06fab-101">Remove-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="06fab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="06fab-102">SYNOPSIS</span></span>
<span data-ttu-id="06fab-103">Remove uma extensão do SQL Server de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="06fab-103">Removes a SQL Server extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06fab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06fab-104">SYNTAX</span></span>

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06fab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="06fab-105">DESCRIPTION</span></span>
<span data-ttu-id="06fab-106">O cmdlet **Remove-AzureRmVMSqlServerExtension** remove uma extensão de servidor AzureSQL de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="06fab-106">The **Remove-AzureRmVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="06fab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="06fab-107">EXAMPLES</span></span>

### <span data-ttu-id="06fab-108">Exemplo 1: remover uma extensão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="06fab-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="06fab-109">Esse comando Remove uma extensão do SQL Server da máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="06fab-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="06fab-110">OS</span><span class="sxs-lookup"><span data-stu-id="06fab-110">PARAMETERS</span></span>

### <span data-ttu-id="06fab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06fab-111">-DefaultProfile</span></span>
<span data-ttu-id="06fab-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="06fab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06fab-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="06fab-113">-Name</span></span>
<span data-ttu-id="06fab-114">Especifica o nome do SQL Server que a extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="06fab-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06fab-115">-ResourceGroupName</span></span>
<span data-ttu-id="06fab-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="06fab-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="06fab-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="06fab-117">-VMName</span></span>
<span data-ttu-id="06fab-118">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="06fab-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06fab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06fab-119">CommonParameters</span></span>
<span data-ttu-id="06fab-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06fab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06fab-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06fab-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06fab-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="06fab-122">INPUTS</span></span>

### <span data-ttu-id="06fab-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="06fab-123">None</span></span>
<span data-ttu-id="06fab-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="06fab-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="06fab-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="06fab-125">OUTPUTS</span></span>

### <span data-ttu-id="06fab-126">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="06fab-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="06fab-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="06fab-127">NOTES</span></span>

## <span data-ttu-id="06fab-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="06fab-128">RELATED LINKS</span></span>

[<span data-ttu-id="06fab-129">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="06fab-129">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="06fab-130">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="06fab-130">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


