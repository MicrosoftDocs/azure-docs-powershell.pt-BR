---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMSqlServerExtension.md
ms.openlocfilehash: 6e3803b7627e16a96c8101f3a6dd1eee5a1b2689
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776902"
---
# <span data-ttu-id="b1c61-101">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b1c61-101">Remove-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="b1c61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1c61-102">SYNOPSIS</span></span>
<span data-ttu-id="b1c61-103">Remove uma extensão do SQL Server de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b1c61-103">Removes a SQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="b1c61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1c61-104">SYNTAX</span></span>

```
Remove-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1c61-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1c61-105">DESCRIPTION</span></span>
<span data-ttu-id="b1c61-106">O cmdlet **Remove-AzVMSqlServerExtension** remove uma extensão de servidor AzureSQL de uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b1c61-106">The **Remove-AzVMSqlServerExtension** cmdlet removes an AzureSQL Server extension from a virtual machine.</span></span>

## <span data-ttu-id="b1c61-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1c61-107">EXAMPLES</span></span>

### <span data-ttu-id="b1c61-108">Exemplo 1: remover uma extensão do SQL Server</span><span class="sxs-lookup"><span data-stu-id="b1c61-108">Example 1: Remove a SQL Server extension</span></span>
```
PS C:\> Remove-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

<span data-ttu-id="b1c61-109">Esse comando Remove uma extensão do SQL Server da máquina virtual chamada ContosoVM22.</span><span class="sxs-lookup"><span data-stu-id="b1c61-109">This command removes a SQL Server extension from the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="b1c61-110">OS</span><span class="sxs-lookup"><span data-stu-id="b1c61-110">PARAMETERS</span></span>

### <span data-ttu-id="b1c61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1c61-111">-DefaultProfile</span></span>
<span data-ttu-id="b1c61-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1c61-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1c61-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1c61-113">-Name</span></span>
<span data-ttu-id="b1c61-114">Especifica o nome do SQL Server que a extensão que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b1c61-114">Specifies the name of the SQL Server the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1c61-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1c61-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1c61-116">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="b1c61-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b1c61-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="b1c61-117">-VMName</span></span>
<span data-ttu-id="b1c61-118">Especifica o nome da máquina virtual a partir da qual esse cmdlet Remove a extensão do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b1c61-118">Specifies the name of the virtual machine from which this cmdlet removes the SQL Server extension.</span></span>

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

### <span data-ttu-id="b1c61-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1c61-119">CommonParameters</span></span>
<span data-ttu-id="b1c61-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1c61-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1c61-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1c61-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1c61-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1c61-122">INPUTS</span></span>

### <span data-ttu-id="b1c61-123">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b1c61-123">None</span></span>
<span data-ttu-id="b1c61-124">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b1c61-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1c61-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1c61-125">OUTPUTS</span></span>

### <span data-ttu-id="b1c61-126">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="b1c61-126">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b1c61-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1c61-127">NOTES</span></span>

## <span data-ttu-id="b1c61-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1c61-128">RELATED LINKS</span></span>

[<span data-ttu-id="b1c61-129">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b1c61-129">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="b1c61-130">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b1c61-130">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


