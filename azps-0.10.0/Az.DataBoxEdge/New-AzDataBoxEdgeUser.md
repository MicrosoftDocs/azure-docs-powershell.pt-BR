---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeUser.md
ms.openlocfilehash: 480c0a8e932b672542595983f33fd19bab6fec3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776753"
---
# <span data-ttu-id="28b97-101">New-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="28b97-101">New-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="28b97-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="28b97-102">SYNOPSIS</span></span>
<span data-ttu-id="28b97-103">Cria um novo usuário para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28b97-103">Creates a new user for the device.</span></span>

## <span data-ttu-id="28b97-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28b97-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -Password <SecureString> -EncryptionKey <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [[-Type] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b97-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="28b97-105">DESCRIPTION</span></span>
<span data-ttu-id="28b97-106">O cmdlet **New-AzDataBoxEdgeUser** cria um novo usuário para o dispositivo de borda da caixa de dados.</span><span class="sxs-lookup"><span data-stu-id="28b97-106">The **New-AzDataBoxEdgeUser** cmdlet creates a new user for the Data Box Edge device.</span></span> <span data-ttu-id="28b97-107">Só há suporte para a criação de usuários do tipo `Share` .</span><span class="sxs-lookup"><span data-stu-id="28b97-107">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="28b97-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="28b97-108">EXAMPLES</span></span>

### <span data-ttu-id="28b97-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="28b97-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

```powershell
PS C:\> New-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
 -Password password-secured-string -EncryptionKey encryption-key -Type Share
User name   Type  ResourceGroupName DeviceName
---------   ----  ----------------- ----------
username    Share resourceGroupName deviceName
```

## <span data-ttu-id="28b97-110">OS</span><span class="sxs-lookup"><span data-stu-id="28b97-110">PARAMETERS</span></span>

### <span data-ttu-id="28b97-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28b97-111">-AsJob</span></span>
<span data-ttu-id="28b97-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="28b97-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28b97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b97-113">-DefaultProfile</span></span>
<span data-ttu-id="28b97-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="28b97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b97-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="28b97-115">-DeviceName</span></span>
<span data-ttu-id="28b97-116">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="28b97-116">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b97-117">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="28b97-117">-EncryptionKey</span></span>
<span data-ttu-id="28b97-118">Chave de criptografia do dispositivo de borda</span><span class="sxs-lookup"><span data-stu-id="28b97-118">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b97-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="28b97-119">-Name</span></span>
<span data-ttu-id="28b97-120">Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="28b97-120">Username</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b97-121">-Senha</span><span class="sxs-lookup"><span data-stu-id="28b97-121">-Password</span></span>
<span data-ttu-id="28b97-122">Senha, fornecer como uma cadeia de caracteres segura</span><span class="sxs-lookup"><span data-stu-id="28b97-122">Password, provide as a secure string</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b97-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b97-123">-ResourceGroupName</span></span>
<span data-ttu-id="28b97-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="28b97-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b97-125">-Digite</span><span class="sxs-lookup"><span data-stu-id="28b97-125">-Type</span></span>
<span data-ttu-id="28b97-126">Selecionar UserType</span><span class="sxs-lookup"><span data-stu-id="28b97-126">Select UserType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b97-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="28b97-127">-Confirm</span></span>
<span data-ttu-id="28b97-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b97-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28b97-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b97-129">-WhatIf</span></span>
<span data-ttu-id="28b97-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="28b97-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28b97-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="28b97-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28b97-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b97-132">CommonParameters</span></span>
<span data-ttu-id="28b97-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b97-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b97-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28b97-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b97-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="28b97-135">INPUTS</span></span>

### <span data-ttu-id="28b97-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="28b97-136">None</span></span>

## <span data-ttu-id="28b97-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="28b97-137">OUTPUTS</span></span>

### <span data-ttu-id="28b97-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="28b97-138">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="28b97-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="28b97-139">NOTES</span></span>

## <span data-ttu-id="28b97-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="28b97-140">RELATED LINKS</span></span>