---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesAccount.md
ms.openlocfilehash: 87febe648a845d595f35c1a14b024fbd97824be1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600776"
---
# <span data-ttu-id="4b41d-101">New-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4b41d-101">New-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="4b41d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b41d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b41d-103">Cria uma nova conta do Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="4b41d-103">Creates a new Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="4b41d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b41d-104">SYNTAX</span></span>

```
New-AzNetAppFilesAccount -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b41d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b41d-105">DESCRIPTION</span></span>
<span data-ttu-id="4b41d-106">O cmdlet **New-AzNetAppFilesAccount** cria uma conta do ANF.</span><span class="sxs-lookup"><span data-stu-id="4b41d-106">The **New-AzNetAppFilesAccount** cmdlet creates an ANF account.</span></span>

## <span data-ttu-id="4b41d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b41d-107">EXAMPLES</span></span>

### <span data-ttu-id="4b41d-108">Exemplo 1: criar uma conta do ANF</span><span class="sxs-lookup"><span data-stu-id="4b41d-108">Example 1: Create an ANF account</span></span>
```
PS C:\>New-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount" -l "westus2"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="4b41d-109">Esse comando cria a nova conta do ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="4b41d-109">This command creates the new ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="4b41d-110">OS</span><span class="sxs-lookup"><span data-stu-id="4b41d-110">PARAMETERS</span></span>

### <span data-ttu-id="4b41d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b41d-111">-DefaultProfile</span></span>
<span data-ttu-id="4b41d-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b41d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b41d-113">-Local</span><span class="sxs-lookup"><span data-stu-id="4b41d-113">-Location</span></span>
<span data-ttu-id="4b41d-114">O local do recurso</span><span class="sxs-lookup"><span data-stu-id="4b41d-114">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b41d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b41d-115">-Name</span></span>
<span data-ttu-id="4b41d-116">O nome da conta do ANF</span><span class="sxs-lookup"><span data-stu-id="4b41d-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b41d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b41d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4b41d-118">O grupo de recursos da conta ANF</span><span class="sxs-lookup"><span data-stu-id="4b41d-118">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b41d-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="4b41d-119">-Tag</span></span>
<span data-ttu-id="4b41d-120">Uma Hashtable que representa as marcas de recursos</span><span class="sxs-lookup"><span data-stu-id="4b41d-120">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b41d-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b41d-121">-Confirm</span></span>
<span data-ttu-id="4b41d-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b41d-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b41d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b41d-123">-WhatIf</span></span>
<span data-ttu-id="4b41d-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b41d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b41d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b41d-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b41d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b41d-126">CommonParameters</span></span>
<span data-ttu-id="4b41d-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b41d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4b41d-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b41d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b41d-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b41d-129">INPUTS</span></span>

### <span data-ttu-id="4b41d-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4b41d-130">None</span></span>

## <span data-ttu-id="4b41d-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b41d-131">OUTPUTS</span></span>

### <span data-ttu-id="4b41d-132">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4b41d-132">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4b41d-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b41d-133">NOTES</span></span>

## <span data-ttu-id="4b41d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b41d-134">RELATED LINKS</span></span>
